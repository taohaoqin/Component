<template>
  <div>
        <button @click="increase">+</button> <button @click="subtract">-</button>
  </div>
</template>
<script>
export default {
    props: {
        count:{
            type:Number,
            default:Infinity
        }
    },
    methods:{
      increase(){
          this.$emit('increase')
      },
      subtract(){
          this.$emit('subtract')
      }
  }
}
</script>

