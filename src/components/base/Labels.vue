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
    font-family: var(--font-mono);
    font-weight: var(--font-regular);
    font-size: 16px;
    color: var(--color-dark);

    border: 1px solid var(--color-black);
    border-radius: 50px;
    padding: 5px 20px;
    box-shadow: 3px 3px 0px var(--color-black);
}

</style>