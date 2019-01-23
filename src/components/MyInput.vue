<template>
  <div>
      <input v-model="count" >
      <MyButton  @increase="getCount"  @subtract="subCount"/>
  </div>
</template>
<script>
import MyButton from "@/components/MyButton.vue";
export default {
    components:{
       MyButton
    },
    data(){
      return{
        count:5
      }
    },
    // computed:{
    //     isNumber:function(){
    //         return parseInt(this.count)
    //     }
    // },
    methods:{
      getCount(){
        if(this.count<10 && this.count>-1){
          this.count++
        }else if(this.count<0){
          this.count=0
        }else{
          this.count=10
        }
      },
      subCount(){
        if(this.count>0 && this.count<11){
          this.count--
        }else if(this.count>10){
          this.count=10
        }else{
          this.count=0
        }
      }
   }
}
</script>


