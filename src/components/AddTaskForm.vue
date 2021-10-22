<template>
    <div class="input-group my-2">
        <input type="text" class="form-control" placeholder="Введите текст задачи..."
               aria-label="Введите текст задачи..." aria-describedby="button-addon2"
               @input="onInputHandler"
               v-model="addTaskInputValue"
        />
        <InputGroupButton
                :icon="iconName"
                :class="buttonSemantics"
                @add-task-form="addNewTask"
        />
    </div>
</template>

<script>
    import InputGroupButton from "@/components/InputGroupButton";

    export default {
        name: "AddTaskForm",
        data() {
            return {
                iconName: 'add',
                buttonSemantics: 'input',
                addTaskInputValue: '',
            }
        },
        props: [],
        components: {
            InputGroupButton
        },
        methods: {
            addNewTask() {
                this.$emit("add-task");
                this.addTaskInputValue = ''
            },
            onInputHandler() {
                this.$emit("change-input-value", this.addTaskInputValue)
            }
        }
    }
</script>

<style scoped>
    .form-control {
        border-color: RGB(128, 128, 128);
    }
    .form-control:focus {
        box-shadow: none;
    }
</style>