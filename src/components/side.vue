<template>
  <div class="side" :style="'top:' + (top+160) +'px;'">
   
  </div>
</template>

<script>
export default {
  name: 'side',
  props:{top:{default:54}},
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style scoped>
  .side{
    position:absolute;
    width:200px;
    height:100px;
    left:100px;
    background-color: yellow;
    transition:.6s;
  }
</style>
