<template>
    <button class="iconButtonSquare"
            @click="$emit('handler')"
    >
        <span class="material-icons">{{icon}}</span>
    </button>
</template>

<script>
    export default {
        name: "IconButtonSquare",
        props: [
            'icon',
        ]
    }
</script>

<style scoped>
    .iconButtonSquare {
        padding: 0;
        border: none;
    }

    .material-icons {
        padding: 0.6875rem;
    }
</style>