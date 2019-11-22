<template>
<div>
<p>いいね{{number}}</p>
<button @click="increment">+1</button>
</div>
</template>

<script>

export default {
  props: ["number"],  //親コンポーネントから子コンポーネントでデータ渡し
  // data : function(){
  //   return {
  //     number:5
  //   }
  // },
  computed: {
    halfNumber() {
      return this.totalNumberl /2;
    }
  },
  methods: {
    increment() {
      this.number+=1;
    }
  }
}
</script>

<style scoped>
div {
  border:1px solid red;
}
</style>
