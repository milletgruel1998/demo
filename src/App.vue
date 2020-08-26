<template>
  <div class="app">
    <h1>我是App页面</h1>
    <!-- <router-link :to="{name:'/Home', params: {name:'小米粥'}}">去home页面</router-link> -->
    <router-link :to="{name:'Home',params}">去home页面</router-link>
    <button @click="changeNum">点击改变数组</button>
    <ul>
      <li v-for="(item,key, index) in obj"
          :key="index">{{key}}---{{item}}</li>
    </ul>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  data () {
    return {
      params: {},
      obj: { name: '小米粥', age: 18 }
    }
  },
  methods: {
    changeNum () {
      // this.arr[1] = 6
      this.$set(this.obj, 'age', 20)
      this.$set(this.obj, 'name', '大米粥')
      console.log('obj', this.obj)
    }
  },
  created () {
    // console.log(this)
    this.params = { name: '小米粥' }
  }
}
</script>

<style>
a {
  text-decoration: none;
  color: #c4c4c4;
  display: block;
  width: 120px;
  height: 50px;
  line-height: 50px;
  border: 1px solid aqua;
  text-align: center;
  cursor: pointer;
}
</style>
