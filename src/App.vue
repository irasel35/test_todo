<template>
  <div id="app">
    <Header />
<Todos v-bind:todos="todos" :xyz="msg"  
            v-on:del-todo="deleteTodo"/>

 </div>
</template>

<script>
import Header from './components/layout/header';
import Todos from './components/Todos';

export default {
  name: 'App',
  components: {
    Todos,
    Header

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
  },
  methods : {
    deleteTodo(id){
this.todos=this.todos.filter(todo=>todo.id !== id)

  }
  }
}
</script>

<style>

</style>
