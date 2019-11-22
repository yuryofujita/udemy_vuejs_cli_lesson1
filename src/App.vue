<template>
<div>
<LikeHeader></LikeHeader>
<p>{{number/2}}</p>
<!-- 
    v-on:my-click="number=$event"→子コンポーネントからの情報をnumberに入れる。
 -->
<LikeNumber v-bind:total-number="number" v-on:my-click="number=$event"></LikeNumber>
<LikeNumber v-bind:total-number="number" test-props="test"></LikeNumber>
</div>
</template>


<script>
import LikeHeader from "./components/LikeHeader.vue";

export default {
    data() {
        return {number:10}
    },
    components : {
        LikeHeader
    }
}
</script>

<style scoped>
div {
    border: 1px solid blue;
}
</style>