<template>
    <ul class="taskList">
        <TaskItem v-for="item of listItems" v-bind:key="item" v-bind:taskItem="item"/>
    </ul>
</template>

<script>
    import TaskItem from "@/components/TaskItem";

    export default {
        name: "TaskList",
        props: [
            'listItems'
        ],
        // data() {
        //     return {
        //         items: 'add',
        //         addTaskInputValue: ''
        //     }
        // },
        components: {
            TaskItem,
        }
    }
</script>

<style scoped>
    .taskList {
        list-style: none;
        padding-left: 0;
    }
</style>