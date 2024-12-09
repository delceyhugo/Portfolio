<script setup>
import Button from './base/Button.vue';

</script>


<template>
    <section id="Hero">
        <article>
            <h1>Hello, je m’appelle Hugo.</h1>
            <h2>développeur web</h2>
            <p>
                Développeur curieux et polyvalent, je me spécialise en Frontend tout en explorant le Backend avec JavaScript et PHP.
            </p>
            <Button>On discute ?</Button>
        </article>
        <aside>
            <img src="@/assets/avatar.png" alt="Mon avatar"/>
        </aside>
    </section>
</template>


<style lang='scss' scoped>

section{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 20px;
    article{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 15px;
        flex: 1;
        @media screen and (max-width: 1000px) {
            align-items: stretch;
            h1{
                font-size: 18px !important;
                font-weight: var(--font-regular) !important;
                text-align: center;
            }
            h2{
                font-size: 50px !important;
                text-align: center;
            }
            p{
                font-size: 18px !important;
                font-weight: var(--font-regular) !important;
                text-align: center;
            }
        }
        h1{
            font-family: var(--font-grotesk);
            font-weight: var(--font-medium);
            font-size: 29px;
            line-height: normal;
            color: var(--color-dark-light);
        }
        h2{
            font-family: var(--font-code);
            font-weight: 900;
            font-size: 96px;
            line-height: normal;
            color: var(--color-dark);
            text-transform: uppercase;
        }
        p{
            font-family: var(--font-grotesk);
            font-weight: var(--font-medium);
            font-size: 29px;
            line-height: normal;
            color: var(--color-dark-light);
        }
    }
    aside{
        display: flex;
        flex: 1;
        justify-content: center;
        img{
            height: 100%;
            width: auto;
            max-width: 80vw;
        }
    }
}

</style>