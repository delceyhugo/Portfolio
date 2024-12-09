<script setup>

</script>


<template>

    <button>
        <slot>
            Button
        </slot>
    </button>

</template>


<style lang='scss' scoped>

    button{
        // Layout
        background-color: var(--color-yellow);
        border: 2px solid var(--color-black);
        border-radius: 12px;
        box-shadow: 4px 4px 0px var(--color-black);
        padding: 10px 30px;
        cursor: pointer;
        // Font
        font-family: var(--font-mono);
        font-weight: var(--font-bold);
        font-size: 29px;
        color: var(--color-dark);
        // Transition
        transition: all 0.1s ease-in-out;
        // Hover
        &:hover{
            filter: contrast(130%);
        }
        // Active
        &:active{
            transform: translate(4px, 4px);
            box-shadow: 0px 0px 0px var(--color-black);
        }
        @media screen and (max-width: 768px){
            // Font
            font-size: 18px;
        }
    }


</style>