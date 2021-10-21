<template>
    <IconButtonSquare
            :icon="icon"
            :semantics="buttonSemantics"
            @handler="formHandler"/>
</template>

<script>
    import IconButtonSquare from "@/components/IconButtonSquare";

    export default {
        name: "InputGroupButton",
        data() {
            return {
                buttonSemantics: 'inputGroupButton'
            }
        },
        components: {
            IconButtonSquare
        },
        props: [
            'icon'
        ],
        methods: {
            formHandler() {
                this.$emit('add-task-form')
            }
        }
    }
</script>

<style scoped>

</style>