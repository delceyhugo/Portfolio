<script setup>
import Button from './base/Button.vue';

const redirect = (url) => {
    window.location.href = url
}
</script>


<template>
    <section id="Works">
        <h1>Explorations et expérimentations</h1>
        <section >
            <img src="@/assets/projet/path.png" alt="Image d'un projet">
            <img src="@/assets/projet/car.png" alt="Image d'un projet">
            <img src="@/assets/projet/usa.png" alt="Image d'un projet">
            <img src="@/assets/projet/expo.png" alt="Image d'un projet">
            <img src="@/assets/projet/starfield.png" alt="Image d'un projet">
            <img src="@/assets/projet/portfolio.png" alt="Image d'un projet">
            <img src="@/assets/projet/sorting.png" alt="Image d'un projet">
            <img src="@/assets/projet/metaway.png" alt="Image d'un projet">
        </section>
        <Button @click="redirect('https://github.com/delceyhugo')">Pour plus de projets, rendez-vous sur Github</Button>
    </section>

</template>


<style lang='scss' scoped>
#Works{
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 50px;
    max-width: 2000px;
    margin: auto;
    h1{
        text-align: center;
    }
    section{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        gap: 35px;
        padding: 0px;
        flex-wrap: wrap;
        max-width: 1300px;
        margin: auto auto 200px auto;

        img{
            width: 400px;
            border-radius: 200px;
            border: 2px solid var(--color-black);
            box-shadow: 4px 4px 0px var(--color-black);
            margin: 0px -75px -150px -75px;
            transition: all 0.15s ease-in-out;
            cursor: pointer;
            &:hover{
                box-shadow: 8px 8px 0px var(--color-black);
                transform: translate(-4px, -4px);
            }
            &:active{
                box-shadow: 0px 0px 0px var(--color-black);
                transform: translate(4px, 4px);
            }
        }
    }
}

</style>