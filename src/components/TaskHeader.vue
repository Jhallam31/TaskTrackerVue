<template>
    <header>
        <h1>{{title}}</h1>
        <TaskButton @btn-click="$emit('toggle-add-task')" :text ="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red' : 'green'"/>
    </header>
</template>
<script>
import TaskButton from "./TaskButton";
    export default{
        name: 'TaskHeader',
        props: {
            title: String,
            showAddTask: Boolean
        },
        components: {
            TaskButton
        }
    }
</script>
<style>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }   
</style>