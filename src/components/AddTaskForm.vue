<template>
    <div class="input-group mb-3">
        <input type="text" class="form-control" placeholder="Введите текст задачи..." aria-label="Введите текст задачи..." aria-describedby="button-addon2"
               @input="onInputHandler"
               v-model="addTaskInputValue"
        />
        <InputGroupButton
                :icon="iconName"
                @add-task-form="addNewTask"
        />
<!--        <button class="btn btn-outline-secondary" type="button" id="button-addon2">Button</button>-->
    </div>
</template>

<script>
    import InputGroupButton from "@/components/InputGroupButton";
    export default {
        name: "AddTaskForm",
        data() {
          return {
              iconName: 'add',
              addTaskInputValue: ''
          }
        },
        props: [
          // 'formValue'
        ],
        components: {
            InputGroupButton
        },
        methods: {
            addNewTask() {
                this.$emit("add-task")
            },
            onInputHandler() {
                // if (this.formValue === '') {
                //     this.addTaskInputValue = this.formValue
                // }
                this.$emit("change-input-value", this.addTaskInputValue)
            }
        }
    }
</script>

<style scoped>

</style>