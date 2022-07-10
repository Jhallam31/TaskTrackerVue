<template>
    <header>
        <h1>{{title}}</h1>
        <TaskButton text ="Add Task" color="green"/>
    </header>
</template>
<script>
import TaskButton from "./TaskButton";
    export default{
        name: 'TaskHeader',
        props: {
            title: String
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