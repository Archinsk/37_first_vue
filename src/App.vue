<template>
    <div id="app" class="container">
        <Header/>
        <AddTaskForm
                @add-task="addNewTask"
                @change-input-value="changeInputValue"
                :formValue="inputValue"
        />
        <TaskList
            :listItems="items"
        />
    </div>
</template>

<script>
    import Header from "@/components/Header";
    import AddTaskForm from "@/components/AddTaskForm";
    import TaskList from './components/TaskList'

    export default {
        name: 'App',
        data() {
            return {
                items: [
                    {id: 1, task: 'Построить дом', done: false, icon: 'stars'},
                    {id: 2, task: 'Посадить дерево', done: true, icon: 'favorite'},
                    {id: 3, task: 'Вырастить сына', done: false, icon: 'home'},
                ],
                inputValue: ''
            }
        },
        components: {
            Header, AddTaskForm, TaskList
        },
        methods: {
            addNewTask() {
                let newTask = {id: this.items.length + 1, task: this.inputValue, done: false, icon: 'home'};
                this.items.push(newTask);
                this.inputValue = "";
            },
            changeInputValue(inputText) {
                this.inputValue = inputText
            }
        }
    }
</script>

<style>
    body {
        background-color: RGB(228, 244, 224);
    }

    #app {
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        background-color: RGB(228, 244, 224);
    }
</style>
