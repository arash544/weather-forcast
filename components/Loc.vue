<template>
<div class="row">
    <div class="col city d-flex justify-content-center align-items-center ">
        <h2>{{ cit }}</h2>
    </div>
</div>
</template>

<script>
export default {
    name: "Loc",
    props: {
        cit: {
            type: String,
            required: true
        }
    }
    // created() {
    //     console.log(this.cit)
    // }
};
</script>

<style lang="scss" scoped>
.city {
    margin-top: 100px;

    h2 {
        font-size: 82px;
        font-weight: 200;
    }
}
</style>
