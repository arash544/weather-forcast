<template>
<div class="row img">
    <div class="col  d-flex justify-content-center align-items-center">
        <img :src="pic" alt="">
    </div>
</div>
</template>

<script>
export default {
    name: "Forcast",
    props: {
        pic: {
            type: String,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>
.img {
    margin-top: 70px;

    @media screen and (max-width:1024px) {
        margin-top: 100px;
    }

    @media screen and (max-width:450px) {
        margin-top: 0px
    }

    img {
        width: 170px;
        height: 170px;
        background-color: transparent;
    }
}
</style>
