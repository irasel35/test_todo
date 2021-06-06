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
        title:"todo One",
        completed:false
         
      },
       {
        id:2,
        title:"todo Two",
        completed:true
         
      },
       {
        id:3,
        title:"todo three",
        completed:false
         
      }
    ]
    }
  }
}
</script>

<style>

</style>
