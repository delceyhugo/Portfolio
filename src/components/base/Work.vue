<script setup>
import Link from './Link.vue';
import Labels from './Labels.vue';
const redirect = (url) => {
    window.location.href = url
}
</script>


<template>
    <article>
        <aside>
            <slot name="icon">
                <img src="@/assets/works/Positivus.png" alt="Interface web">
            </slot>
        </aside>
        <header>
            <h2>
                <slot name="title">
                    Positivus
                </slot>
            </h2>
            <slot name="labels">
                <Labels color="var(--color-blue)">
                    Vue
                </Labels>
            </slot>
        </header>
        <p>
            <slot name="text">
                Ce projet est une démonstration de mes compétences en <strong>intégration web</strong>, de la conception à la publication, en passant par l'optimisation.
            </slot>
        </p>
        <slot name="link">
            <Link @click="redirect('https://positivus-demo.netlify.app')">Voir le projet</Link>
        </slot>
    </article>
</template>


<style lang='scss' scoped>

article{
    // Layout
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    padding: 20px 30px;
    max-width: 500px;
    flex: 1;

    // Style
    border: 2px solid var(--color-black);
    border-radius: 12px;
    box-shadow: 4px 4px 0px var(--color-black);
    background-color: var(--color-white);
    transition: all 0.15s ease-in-out;

    &:hover{
        box-shadow: 8px 8px 0px var(--color-black);
        transform: translate(-4px, -4px);
    }

    aside{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        margin: auto;
        border: 2px solid var(--color-black);
        border-radius: 12px;
        box-shadow: 2px 2px 0px rgba(0, 0, 0, 0.5);
        background-color: var(--color-blue);
        overflow: hidden;
        width: 100%;
        img{
            width: 100%;
        }
    }
    header{
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 5px;
        justify-content: space-between;
        width: 100%;
        h2{
            flex: 1;
        }
    }
    >p{
        flex: 1;
        min-width: 300px;
    }
}

</style>