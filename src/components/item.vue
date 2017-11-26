<template>
        <div class="item" @click="openMe">{{idx}}</div>
</template>

<script>
export default {
  name: 'item',
  props:['idx'],
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
      openMe(){

      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
</style>
