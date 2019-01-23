<template>
  <div class="home">
   
    <MyInput />
  </div>
</template>

<script>
// @ is an alias to /src
import MyInput from '@/components/MyInput.vue'

export default {
  name: 'home',
  components: {
    MyInput
  }
}
</script>
