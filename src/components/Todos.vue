<template>
<div>
   <div v-for="todo in todos" :key="todo.id">
   <!--  <h3 v-if="todo.id%2!=0"> {{todo.title}}</h3>
 -->
    <TodoItem v-bind:todo="todo"  v-on:del-todo="$emit('del-todo',todo.id)"/>
    
   </div>
   
  <!--  <div>
       <h1>{{xyz}}</h1>
   </div> -->
</div>
    
</template>



<script>
import TodoItem from './TodoItem.vue';
export default {
    name: "Todos",
    components:{
        TodoItem
    },
    props: [
        "todos",
        "xyz"
    ]
}
</script>

<style >

</style>