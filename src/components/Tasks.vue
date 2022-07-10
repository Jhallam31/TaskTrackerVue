<template>
    <div>

    <div :key ="task.id" v-for="task in tasks">
        <Task  @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" v-bind:task="task" />
    </div>
    </div>
</template>

<script>
import Task from "./Task";
    export default{
        name: 'Tasks',
        props:{
            tasks: Array
        },
        components:{
            Task
        },
        emits:[
            'delete-task',
            'toggle-reminder'
        ]
    }
</script>
<style scoped>
.add-form {
  margin-bottom: 40px;
}
.form-control {
  margin: 20px 0;
}
.form-control label {
  display: block;
}
.form-control input {
  width: 100%;
  height: 40px;
  margin: 5px;
  padding: 3px 7px;
  font-size: 17px;
}
.form-control-check {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.form-control-check label {
  flex: 1;
}
.form-control-check input {
  flex: 2;
  height: 20px;
}
</style>