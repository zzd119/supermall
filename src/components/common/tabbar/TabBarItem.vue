<template>
    <div class="tab-bar-item">
      <div :style='activeStyle' @click="itemClick"> <slot  name="item-text">首页</slot> </div>
    </div>
</template>

<script>
export default {
   name:"TabBarItem",
   props:{
      path: String,
      activeColor:{
        type:String,
        default: 'red'
      }
   },
   data(){
     return {}
   },
   computed:{
     isActive(){
        return this.$route.path.includes(this.path)
     },
      activeStyle(){
        return this.isActive?{color : this.activeColor} :{}
     }
   },
   methods:{
     itemClick(){
       if(!this.isActive)
       this.$router.replace(this.path)
     }
   }
}
</script>

<style scoped>
   .tab-bar-item{
     flex: 1;
     text-align: center;
     height: 49px;
     line-height: 49px;
   }
   .active{
     color: red;
   }
</style>