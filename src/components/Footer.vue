<script setup>
import Logo from './base/Logo.vue';
import { ref } from 'vue';

const logoCount = ref(5);

//280
const setLogoCount = () => {
    let width = Math.floor(window.innerWidth/150)
    width % 2 == 0 ? logoCount.value = width : logoCount.value = width + 1
}
setLogoCount()
window.addEventListener('resize', setLogoCount)

</script>

<template>
    <footer>
        <div>
            <Logo v-for="i in logoCount" />
        </div>
    </footer>
</template>

<style lang='scss' scoped>
footer{
    // display: flex;
    overflow: hidden;
    width: 100%;
    >div{
        display: flex;
        flex-direction: row;
        width: 200%;
        animation: slide 10s linear infinite;
        @media screen and (max-width: 600px) {
            animation: none;
        }
    }
    @keyframes slide{
        0%{
            transform: translate(0px, 0px);
        }
        100%{
            transform: translate(-50%, 0px);
        }
    }
}

</style>