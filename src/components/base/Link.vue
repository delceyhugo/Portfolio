<script setup>

</script>


<template>
    <button>
        <img width="40" height="40" src="@/assets/link.png" alt="circled-up-right-2">
        <slot>
            Link
        </slot>
    </button>
</template>


<style lang='scss' scoped>
button{
    // Layout
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 8px;
    cursor: pointer;

    // Style
    background-color: transparent;
    border: none;
    color: var(--color-black);
    font-family: var(--font-grotesk);
    font-weight: var(--font-medium);
    font-size: 18px;
    line-height: 25px;
    text-decoration: none;
    
    &:hover{
        text-decoration: underline;
        & img{
            box-shadow: 4px 4px 0px #00000075;
            transform: translate(-2px, -2px);
        }
    }
    &:active{
        & img{
            transform: translate(4px, 4px);
            box-shadow: 0px 0px 0px var(--color-black);
        }
    }
    img{
        transition: all 0.15s ease-in-out;
        border-radius: 20px;
        box-shadow: 2px 2px 0px #00000075;

    }
}

</style>    