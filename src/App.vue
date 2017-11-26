<template>
  <div class="main">
      <div class="head">{{name}}    
      </div>
      <div class="body">
          <!--<item v-for="(item,idx) in arr" :idx='idx' :key="idx"></item>-->
          <div class="item" v-for="(item,idx) in arr" @click="click(idx)" :key="idx">{{idx}}/{{item}}</div>

      </div>
      <side :top="top"> </side>  
  </div>
</template>

<script>
import side from './components/side'
import item from './components/item'

export default {
  name: 'app',
  data(){
    return{
      top:0,
        name:'ilan',
        arr:['wwwwwww','rrr','trt','rtrt','hjhj','hjdfh','dsrbr','srbyery','rtby','ertv3w','evtre','ertve','evtet'],
    }
  },
  methods:{
click(idx){
  let top = document.getElementsByClassName('item')[idx].offsetTop;
    console.log('idx',top);

  this.top = top;
}
  },
  components: {
    side,item
  }
}
</script>

<style>
 .head{
        width:100%;
        height:140px;
        background-color: blue;
        position:fixed;
        z-index: 2;
    }
    .body{
      position:relative;
      top:150px;
      width:100%;
      background-color: lightgray;
    }
    .item{
        width:100px;
        height:70px;
        background-color: green;
        border:1px solid red;
        margin-bottom:20px;
        font-size: 25px;
        cursor: pointer;
  }
</style>
