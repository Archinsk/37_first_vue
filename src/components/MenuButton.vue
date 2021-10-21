<template>
    <IconButtonSquare :icon="icon" :semantics="buttonSemantics"/>
</template>

<script>
    import IconButtonSquare from "@/components/IconButtonSquare";

    export default {
        name: "MenuButton",
        data() {
            return {
                buttonSemantics: 'menuButton'
            }
        },
        components: {
            IconButtonSquare
        },
        props: [
            'icon'
        ]
    }
</script>

<style scoped>
    .iconButtonSquare {
        margin-left: 0.75rem;
    }
</style>