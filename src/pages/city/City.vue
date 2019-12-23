<template>
    <div>
        <city-header></city-header>
        <city-search :cities='cities'></city-search>
        <!-- 将axios获得的json数据cities,hotCities传递给List局部组件 -->
        <!-- 将letter参数在传递给List局部组件 -->
        <city-list :cities="cities" 
                    :hot="hotcities"
                    :letter='letter'></city-list>
        <!-- 将axios获取的json数据cities传递给alphabet局部组件 -->
        <city-alphabet :cities="cities"
                        @change='handleLetterChange'>
                     <!-- 监听Alphabet组件里的change事件  -->
        </city-alphabet>
    </div>
</template>

<script>
import CityHeader from "./components/Header"
import CitySearch from "./components/Search"
import CityList from "./components/List"
import CityAlphabet from "./components/Alphabet"
import axios from 'axios'

export default {
    name: "City",
    components: {
        CityHeader,
        CitySearch,
        CityList,
        CityAlphabet
    },
    // 通过data初始化数据
    data () {
        return {
            cities: {},
            hotcities: [],
            letter: ''
        }
    },
    // 通过getCityInfo函数获取city.json里的数据，然后传递给handleGetCityInfoSucc函数
    methods: {
        getCityInfo () {
           axios.get('/api/city.json').then(this.handleGetCityInfoSucc)      
        },
        handleGetCityInfoSucc (res) {
            res = res.data
            if (res.ret && res.data) {
                const data = res.data
                this.cities = data.cities
                this.hotcities = data.hotCities
            }
            //  console.log(res)
        },
        handleLetterChange (letter) {
            this.letter = letter
            // console.log(letter)
        }

    },
    // 在生命周期里调用getCityInfo函数
    mounted () {
        this.getCityInfo()
    }
}
</script>