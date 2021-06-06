<template>
  <div class="hello">
  
    <h1>{{input}}</h1>
    <h1>{{name}}</h1>
   
    
  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data:function(){
    return{
      name:"The name is"
    }
  },
  data1:function(){
    return{
      input:"the name"

    }
    
  },
  props: {
    msg: String
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
