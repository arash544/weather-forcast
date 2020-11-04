<template>
<div class="row icons d-flex justify-content-center align-items-center ">
    <Iconshape photo="sun.svg" txt="Sunrise" :num="condition.feelslike" />
    <Iconshape photo="wind.svg" txt="Wind" :num="condition.wind_speed" />
    <Iconshape photo="pre.svg" txt="Pressure" :num="condition.pressure" />
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
}
</style>
