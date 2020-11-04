<template>
<div class="banner">
    <div class="container-fluid" v-if="weather">
        <Loc :cit="weather.location.name" />
        <Times :times="weather.location.localtime" />
        <Forcast pic="http://openweathermap.org/img/wn/04d@2x.png" />
        <Temp :temp="weather.current.temperature" />
        <Situation :sit="weather.current.weather_descriptions[0]" :cits="weather.location.name" />
        <Icons :condition="weather.current" />
    </div>
</div>
</template>

<script>
import axios from "axios";
import Loc from "@/components/Loc";
import Times from "@/components/Times";
import Forcast from "@/components/Forcast";
import Temp from "@/components/Temp";
import Situation from "@/components/Situation";
// import Iconshape from '@/components/icon-part/Iconshape'
import Icons from '@/components/icon-part/Icons'
export default {
    component: {
        Loc,
        Times,
        Forcast,
        Temp,
        Situation,
        // Iconshape
        Icons
    },
    data() {
        return {
            weather: ""
        };
    },
    created() {
        axios
            .get(
                "http://api.openweathermap.org/data/2.5/weather?q=vienna&appid=be8952e8d9a144b625f22b737368de07"
            )
        axios
            .get(
                "http://api.weatherstack.com/current?access_key=fa81e213f450fa1a269b4077eb25d6d9&query=Vienna"
            )
            .then(rs => {
                console.log(rs.data);
                this.weather = rs.data;
                console.log(this.weather.weather[0].icon);
            });
    }
};
</script>

<style lang="scss" scoped>
.container-fluid {
    padding-left: 0;
    padding-right: 0;
}

.banner {
    background: url("/sky.jpg");
    min-height: 100vh;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
}
</style>
