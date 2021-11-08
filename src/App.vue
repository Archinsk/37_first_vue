<template>
    <div id="app">
        <Header/>
        <div class="container">
            <AddTaskForm
                    @add-task="addNewTask($event)"
            />
            <TaskList
                    :listItems="items"
            />
        </div>
        <BootstrapButton type="reset"/>
        <BootstrapButton semantic="danger"/>
        <BootstrapButton type="menu" semantic="success" outline/>

        <IconButtonSquare icon="home"/>
    </div>
</template>

<script>
    import Header from "@/components/Header";
    import AddTaskForm from "@/components/AddTaskForm";
    import TaskList from '@/components/TaskList'
    import BootstrapButton from "@/components/BootstrapButton";
    import IconButtonSquare from "@/components/universal/IconButtonSquare";

    export default {
        name: 'App',
        data() {
            return {
                items: [
                    {id: 1, task: 'Построить дом', done: false, icon: 'stars'},
                    {id: 2, task: 'Посадить дерево', done: true, icon: 'favorite'},
                    {id: 3, task: 'Вырастить сына', done: false, icon: 'home'},
                ],
                // inputValue: ''
            }
        },
        components: {
            Header,
            AddTaskForm,
            TaskList,
            BootstrapButton,
            IconButtonSquare,
        },
        methods: {
            addNewTask(event) {
                let newTask = {id: this.items.length + 1, task: event, done: false, icon: 'home'};
                this.items.push(newTask);
                this.inputValue = "";
            },
            // changeInputValue(inputText) {
            //     this.inputValue = inputText
            // }
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
