<template>
<div class="row city">
    <div class="col  d-flex justify-content-center align-items-center ">
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
    padding-top: 100px;

    @media screen and (max-width:450px) {
        padding-top: 0px
    }

    h2 {
        font-size: 82px;
        font-weight: 200;
    }
}
</style>
