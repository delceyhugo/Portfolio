<script setup>
import Link from './Link.vue';

</script>


<template>
    <article class="anim-from-center">
        <aside>
            <slot name="icon">
                <img src="@/assets/icon/interface.png" alt="Icon d'interface web">
            </slot>
        </aside>
        <h2>
            <slot name="title">
                Côté client
            </slot>
        </h2>
        <p>
            <slot name="text">
                Je donne vie à des sites web grâce à l'intégration d’interfaces modernes et dynamiques.
                <br>
                <br>
                De l’integration de maquettes à celle fonctionnalités interactives, je maîtrise HTML, CSS, JavaScript, Sass, Vue.js, React, jQuery, GSAP, Bootstrap, et bien plus.
                <br>
                <br>
                Que ce soit pour un design responsive, des animations sur mesure ou un SEO optimisé, je m’assure que mon projet se démarque.
            </slot>
        </p>
        <Link>Voir les projets</Link>
    </article>

</template>


<style lang='scss' scoped>
article{
    // Layout
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex: 1;
    gap: 15px;
    padding: 20px 30px;
    max-width: 500px;

    // Style
    border: 2px solid var(--color-black);
    border-radius: 12px;
    box-shadow: 4px 4px 0px var(--color-black);
    background-color: var(--color-white);
    transition: all 0.15s ease-in-out;

    @media screen and (max-width: 500px) {
        max-width: 90%;
        p{
            min-width: fit-content !important;
        }
    }

    &:hover{
        box-shadow: 8px 8px 0px var(--color-black);
        transform: translate(-4px, -4px);
    }

    aside{
        border: 2px solid var(--color-black);
        border-radius: 50px;
        box-shadow: 4px 4px 0px var(--color-black);
        background-color: var(--color-blue);
        width: 100px;
        height: 100px;
        overflow: hidden;
    }
    p{
        flex: 1;
        min-width: 300px;
    }
}

</style>