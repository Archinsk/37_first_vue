<template>
    <button :type="btnType" :class="btnClass">Button</button>
</template>

<script>
    export default {
        name: "BootstrapButton",
        props: {
            type: String,
            semantic: String,
            outline: Boolean,
        },
        computed: {
            btnType: function () {
                let buttonType = "button";
                if (this.type === "submit" || this.type === "reset" || this.type === "menu") {
                    buttonType = this.type
                }
                return buttonType
            },
            btnClass: function () {
                let buttonClass = "btn";
                if (this.semantic) {
                    buttonClass += " btn-"
                    if (this.outline) {
                        buttonClass += "outline-"
                    }
                    buttonClass += this.semantic
                }
                return buttonClass
            },

        }
    }
</script>

<style scoped>

</style>