<template>
<div>
<p>いいね{{halfNumber}}</p>
<button @click="increment">+1</button>
</div>
</template>

<script>

export default {
  //props: ["number"],  //親コンポーネントから子コンポーネントでデータ渡し
  // props: ["totalNumber"],  //親コンポーネントから子コンポーネントでデータ渡し
  props: {
    totalNumber: {
      type:Number, //型
      required: true,  //属性が必須かどうか
      default:5,
    },
    testProps:{
      type:String,
    }
  },
  // data : function(){
  //   return {
  //     number:5
  //   }
  // },
  computed: {
    halfNumber() {
      return this.totalNumber /2;
    }
  },
  methods: {
    increment() {
      // this.number+=1;
      //子コンポーネントから親にデータを渡す。
      //親コンポーネントにv-on:my-click="$event"を指定
      this.$emit("my-click", this.totalNumber+1)
    }
  }
}
</script>

<style scoped>
div {
  border:1px solid red;
}
</style>
