<template>
  <div id="app">
<Todos v-bind:todos="todos" :xyz="msg" />

 </div>
</template>

<script>
import Todos from './components/Todos';

export default {
  name: 'App',
  components: {
    Todos

  },
  data(){
    return {
     msg:'rasel' ,
    todos: [
      {
        id:1,
        title:"Todo One",
        completed:true
         
      },
       {
        id:2,
        title:"Todo Two",
        completed:true
         
      },
       {
        id:3,
        title:"Todo three",
        completed:false
         
      }
    ]
    }
  }
}
</script>

<style>

</style>
