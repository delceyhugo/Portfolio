<script setup>

defineProps({
    color: {
        type: String,
        default: 'var(--color-yellow)'
    }
})
</script>


<template>
    <p :style="{background: color}">
        <slot>
            Labels
        </slot>
    </p>
</template>


<style lang='scss' scoped>
p{
    // Font
    font-family: var(--font-mono);
    font-weight: var(--font-regular);
    font-size: 16px !important;
    color: var(--color-dark);

    // Layout
    border-radius: 50px;
    padding: 5px 20px;

    // Style
    border: 1px solid var(--color-black);
    box-shadow: 3px 3px 0px var(--color-black);
    transition: all 0.15s ease-in-out;

    &:hover{
        box-shadow: 6px 6px 0px var(--color-black);
        transform: translate(-3px, -3px);
        background-color: var(--color-dark) !important;
        color: var(--color-white);
    }
}

</style>