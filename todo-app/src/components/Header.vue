<template>
    <header>
        <h1>{{title}}</h1>
        <Button @toggle-add-task="$emit('toggle-add-task')" text="Add Task" color="green"/>
    </header>
</template>

<script>

// Adding props to components two ways to let the componanet know there's props

// inside the export default:
//     props:['name_of_props', ...]
//     or 
//     props:{title: String}
//     or 
//     props: {title:{
//         type:String,
//         default: 'default value for prop'
//     }}

    import Button from './Button'

    export default {
        name: 'Header',
        props: {
            title: {
                type: String, 
                default: 'Hello World'
            }
        },
        components: {
            Button
        }
    }
</script>

<style scoped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>