<template>
<div class="row temp">
    <div class="col  d-flex justify-content-center align-items-center">
        <h3>{{temp}}°c</h3>
    </div>
</div>
</template>

<script>
export default {
    name: "Temp",
    props: {
        temp: {
            type: Number,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>
.temp {
    margin-top: 70px;

    @media screen and (max-width:450px) {
        margin-top: 0px
    }

    h3 {
        font-weight: 300;
        font-size: 72px
    }
}
</style>
