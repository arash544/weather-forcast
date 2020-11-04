<template>
<div class="row sit">
    <div class="col  d-flex flex-column justify-content-center align-items-center">
        <h6>{{ sit }}</h6>
        <h6>{{ cits }}</h6>
    </div>
</div>
</template>

<script>
import Loc from "./Loc";
export default {
    name: "Situation",
    component: {
        Loc
    },
    props: {
        sit: {
            type: String,
            required: true
        },
        cits: {
            type: String,
            required: true
        }
    },
    created() {
        console.log(this.sit);
    }
};
</script>

<style lang="scss" scoped>
.sit {
    margin-top: 10px;

    h6 {
        font-size: 16px;
        font-weight: 200;
    }
}
</style>
