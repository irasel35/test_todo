<template>
  <div id="app">
    <Header />
    <AddTodo v-on:add-todo="addTodo"/>
  <Todos v-bind:todos="todos" :xyz="msg"  
            v-on:del-todo="deleteTodo"/>

 </div>
</template>

<script>
import AddTodo from './components/AddTodo';
import Header from './components/layout/header';
import Todos from './components/Todos';

export default {
  name: 'App',
  components: {
    Todos,
    Header,
    AddTodo

  },
  data(){
    return {
     msg:'rasel' ,
    todos: [
      {
        id:1,
        title:"Todo One",
        completed:false
         
      },
       {
        id:2,
        title:"Todo Two",
        completed:false
         
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

  },
  addTodo(newTodo){
    this.todos=[...this.todos, newTodo]; 
    //adding new member in array
  }
  }
}
</script>

<style>
.sbmt-btn{
  display: inline;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
  /* text-align: left; */
}

</style>
