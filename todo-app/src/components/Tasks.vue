<template>
    <div>
        <div :key="task.id" v-for="task in tasks" >
        <!-- brings the function from Task up into Tasks so that it can be sent to App -->
        <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
    </div>
    </div>
</template>

<script>

import Task from './Task'

export default {
    name: 'Tasks',
    props:{
        tasks: Array
    },
    components:{
        Task
    },
    emits: ['delete-task']
}
</script>