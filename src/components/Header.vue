<template>
    <header>
        <img id="logo" src="img/lifeplan_logo.jpg" alt="">
        <div>
            <MenuButton :icon="menu"/>
            <MenuButton :icon="logout"/>
        </div>
    </header>
</template>

<script>
    import MenuButton from "@/components/MenuButton";

    export default {
        name: "Header",
        data() {
            return {
                menu: 'menu',
                logout: 'logout',
            }
        },
        components: {
            MenuButton
        }
    }
</script>

<style scoped>
    header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        background-color: RGB(96, 192, 96);
        color: white;
    }

    #logo {
        height: 4.5rem;
    }

    ul {
        list-style: none;
        padding-left: 0;
    }
</style>