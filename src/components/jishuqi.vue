<template>
  <div class="conten-jishu">
    <input type="button" value="+" @click="jia">
    <span>{{num}}</span>
    <input type="button" value="-" @click="jian">
  </div>
</template>
<script>
export default {
  name: "jishu",
//   父传子 props接收
  props:['initnum','dfmax','dfmin','bushu'],
  //   数据
  data() {
    return {
      num: 10,
      min:1,
      max:25,
    initbshu:2
    };
  },
  created() {
      if(this.initnum){
            this.num=this.initnum;
      };
      if(this.dfmax){
    this.max=this.dfmax
      };
      if(this.dfmin){
          this.min=this.dfmin
      };
      if(this.bushu){
          this.initbshu=this.bushu
      }
  },
  //   方法
  methods: {
    jia() {
        this.num+=this.initbshu
        if(this.num>this.max)
      this.num=this.max
    },
    jian() {
        this.num-=this.initbshu
        if(this.num<this.min){
               this.num=this.min
        }
    }
  }
};
</script>
<style lang="scss">
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height:800px;
  .conten-jishu {
    width: 150px;
    input{
        width: 50px;
        height: 100%;
    }
    span{
        display: inline-block;
        text-align: center;
        width: 50px;
         height: 100%;
    }
  }
}
</style>