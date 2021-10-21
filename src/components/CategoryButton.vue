<template>
    <IconButtonSquare :icon="icon" :semantics="buttonSemantics"/>
</template>

<script>
    import IconButtonSquare from "@/components/IconButtonSquare";

    export default {
        name: "CategoryButton",
        data() {
            return {
                buttonSemantics: 'categoryButton'
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
        margin-right: 0.75rem;
        border-radius: 0.1875rem 0;
        background-color: deepskyblue;
        color: RGB(240, 255, 224);
    }
</style>