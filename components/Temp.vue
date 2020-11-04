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

    h3 {
        font-weight: 300;
        font-size: 72px
    }
}
</style>
