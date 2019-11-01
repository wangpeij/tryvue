<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul>
      <li>爱的纸:{{a}}</li>
      <li v-bind:id="'list'+b">{{b}}</li>
      <li v-once>v-once:{{b}}</li>
      <li ><span v-html="b"></span></li>
      <li v-once>bidezhi:{{b}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome',
      a:new Date().getTime(),
      b:3323,
    }
  },
  beforeCreate:function(){
    console.log('beforecreate')
  },
  created:function(){
    console.log('created')
  },
  beforeMount:function(){
    console.log('beforeMount')
  },
  mounted:function(){
     console.log('mounted')
  },
  beforeUpdate:function(){
    console.log('beforeUpdate')
  },
  updated:function(){
    console.log('updated')
  },
  beforeDestroy:function(){
    console.log('beforeDestroy')
  },
  destroyed:function(){
    console.log('destroyed')
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
