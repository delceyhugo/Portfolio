<script setup>

</script>


<template>
    <div>
        <img draggable="false" src="@/assets/logo.svg" alt="Logo">
        <h1>hugo.delcey</h1>
    </div>
</template>


<style lang='scss' scoped>
    div{
        display: flex;
        flex: 1;
        flex-direction: row;
        align-items: center;
        gap: 14px;
        padding: 5px 30px;
        img{
            width: 29px;
            height: auto;
        }
        h1{
            font-family: var(--font-grotesk);
            font-size: 29px;
            font-weight: var(--font-bold);
            color: var(--color-dark);
            user-select: none;
        }
    }
</style>