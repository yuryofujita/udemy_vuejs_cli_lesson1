<template>
<div>
<LikeHeader>
    <h2>みなさん</h2>
    <template v-slot:title="slotProps">
        <h2>こんにちは</h2>
        <h2>{{slotProps}}</h2>
        <h2>{{slotProps.user.firstName}}</h2>
    </template>
    <h3>初めまして</h3>
    <p>よろしくお願いいたします。</p>
    <template v-slot:number>
        <h2>{{number}}</h2>
    </template>
</LikeHeader>
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