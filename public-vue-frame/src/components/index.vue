<template>
  <div class="index">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <div><router-link to="/test">jump</router-link></div>
    
   
  </div>
</template>

<script>
  import {get} from "../utils/request.js"
export default {
  name: 'index',
  data(){
    return{
      msg:'hellohello'
    }
  },
  mounted(){
    //更新时间
    this.get(host.url+'/newtime').then((res)=>{
      console.log(res)
    })
  },
  methods:{
    get,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
