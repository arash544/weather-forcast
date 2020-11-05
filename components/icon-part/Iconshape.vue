<template>
<div class="col-4 flex-column d-flex justify-content-center align-items-center">
    <img :src="photo" alt="">
    <h6>{{txt}}</h6>
    <span>{{num}} <span v-if="wind"> m/s</span><span v-if="pressure">°</span></span>

</div>
</template>

<script>
export default {
    name: "Iconshape",
    props: {
        photo: {
            type: String,
            required: true
        },
        txt: {
            type: String,
            required: true
        },
        num: {
            type: Number,
            required: true
        },
        wind: {
            // type: String,
            // required: true
        },
        pressure: {
            // type: String,
            // required: true
        },
    }
}
</script>

<style lang="scss" scoped>
img {
    margin-bottom: 20px;
}

span {
    font-weight: 200
}
</style>
