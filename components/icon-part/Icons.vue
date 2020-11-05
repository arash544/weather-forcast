<template>
<div class="row icons d-flex justify-content-center align-items-center ">
    <Iconshape photo="sun.svg" txt="Sunrise" :num="condition.feelslike" />
    <Iconshape photo="wind.svg" txt="Wind" :num="condition.wind_speed" wind="true" />
    <Iconshape photo="pre.svg" txt="Pressure" :num="condition.pressure" pressure="true" />
</div>
</template>

<script>
import Iconshape from './Iconshape'
export default {
    name: "Icons",
    component: {
        Iconshape
    },
    props: {
        condition: {
            type: Object,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>
.icons {
    margin-top: 50px;
    padding-bottom: 50px;

    @media screen and (max-width:1024px) {
        margin-top: 200px;
    }

    @media screen and (max-width:450px) {
        margin-top: 0px;
    }
}
</style>
