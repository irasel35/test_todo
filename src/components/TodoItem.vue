<template>
    <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete" name="" id="">
           {{todo.title}}
        </p>
    </div>
</template>
<script>
export default {
    name:"TodoItem",
    props:["todo"],
    methods:{
        markComplete(){
            console.log(123)
        }
    }
}
</script>


<style scoped>
.todo-item {
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #CCC dotted;
}
.is-complete {
    text-align: center;
    text-decoration: line-through;
}
.del {
    background: chartreuse;
}

</style>