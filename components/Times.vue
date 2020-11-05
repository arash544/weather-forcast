<template>
<div class="row">
    <div class="col  d-flex justify-content-center align-items-center">
        <h6 class="time">{{times}}</h6>
    </div>
</div>
</template>

<script>
export default {
    name: "Times",
    props: {
        times: {
            type: String,
            required: true,
        }
    }
}
</script>

<style lang="scss" scoped>
.time {
    // margin-top:20px
    font-size: 20px;
    font-weight: 200;
}
</style>
