<script setup>
import Work from './base/Work.vue';
import Labels from './base/Labels.vue';
import Button from './base/Button.vue';
import Link from './base/Link.vue';

const redirect = (url) => {
    window.location.href = url
}
</script>


<template>
    <section id="Highlight">
        <h1>Ce dont je suis fier</h1>

        <section id="Game">
                <h2>Estate Empire</h2>
                <p id="p1">
                    Estate Empire est mon projet le plus ambitieux et la réalisation d’un rêve d’enfance : concevoir un jeu vidéo de A à Z, et tout ça sans aucune expérience ni connaissance. 
                </p>
                <p id="pz">
                    Avec mon coéquipier, nous avons voulu offrir une expérience soignée, capable de rivaliser avec des projets plus établis, sans laisser deviner qu’il s’agissait d’un travail de débutants.
                </p>
                <p id="p2">
                    Développé sur Unreal Engine 5, <strong>j’ai conçu toutes les interfaces et le level design</strong>, réalisé des modélisations 3D, des textures et shaders, ainsi que l'intégration de fonctionnalités en C++ et Blueprint.
                </p>
                <img src="@/assets/works/estate3.png" alt="Screenshot de Estate Empire">
                <p id="p3">                    
                    J’ai également travaillé sur l’intégration des sons et des musiques, rendant ce jeu une expérience complète et immersive.
                    Ce projet reflète ma passion et ma capacité à mener un projet complexe de bout en bout.
                </p>
                <footer>
                    <Button @click="redirect('https://store.steampowered.com/app/2604670/Estate_Empire/?l=french')" >
                        Page Steam
                    </Button>
                    <Link @click="redirect('https://metaway-studio.com')">
                        Metaway Studio
                    </Link>
                </footer>
        </section>

        <section id="Works">
            <Work />
            <Work>
                <template v-slot:icon>
                    <img width="100%" src="@/assets/works/starryweather.png" alt="image d'interface" />
                </template>
                <template v-slot:title>
                    Starry Weather
                </template>
                <template v-slot:labels>
                    <Labels color="var(--color-red)">
                        React
                    </Labels>
                </template>
                <template v-slot:text>
                    App météo développée avec <strong>React</strong> en composants fonctionnels et avec React Router. <br>
                    Utilisation d’une <strong>api externe</strong>.
                </template>
                <template v-slot:link>
                    <Link @click="redirect('https://starryweather.netlify.app')">
                        Voir le projet
                    </Link>
                </template>
            </Work>
            <Work>
                <template v-slot:icon>
                    <img width="100%" src="@/assets/works/api.png" alt="api" />
                </template>
                <template v-slot:title>
                    Api Auth
                </template>
                <template v-slot:labels>
                    <Labels color="var(--color-teal)">
                        Node.js
                    </Labels>
                </template>
                <template v-slot:text>
                    Api développé avec <strong>Node.js et Express</strong>, utilisant <strong>MongoDB</strong> pour tout sauvegardé sur une base de
                    donnée.
                </template>
                <template v-slot:link>
                    <Link @click="redirect('https://github.com/delceyhugo/User-Authentification-API')">
                        Voir le projet
                    </Link>
                </template>
            </Work>
        </section>
    </section>
</template>


<style lang='scss' scoped>
#Highlight {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 35px;
    #Works {
        display: flex;
        flex-direction: row;
        align-items: stretch;
        flex-wrap: wrap;
        gap: 35px;
        justify-content: center;
        width: 100%;
    }



    #Game{
        // Layout
        display: grid;
        grid-template-areas: 
            "a a"
            "b e"
            "z e"
            "c d"
            "f f";
        grid-template-columns: 1fr 1fr;
        align-items: center;
        gap: 15px;

        max-width: 2000px;

        // Style
        padding: 30px;
        border: 2px solid var(--color-black);
        border-radius: 12px;
        box-shadow: 4px 4px 0px var(--color-black);
        background-color: var(--color-white);
        transition: all 0.15s ease-in-out;

        &:hover{
            box-shadow: 8px 8px 0px var(--color-black);
            transform: translate(-4px, -4px);
        }
        @media screen and (max-width: 1000px) {
            display: flex;
            flex-direction: column;
            align-items: stretch;
            footer{
                flex-wrap: wrap;
            }
        }
        h2{grid-area: a;}
        .p1{grid-area: b;}
        .p2{grid-area: c;}
        .p3{grid-area: d;}
        .pz{grid-area: z;}
        footer{
            grid-area: f;

            display: flex;
            flex-direction: row;
            gap: 10px;
            justify-content: space-between;
        }
        img{
            grid-area: e;
            flex: 1;
            border: 2px solid var(--color-black);
            border-radius: 12px;
            box-shadow: 2px 2px 0px rgba(0, 0, 0, 0.5);
            overflow: hidden;
            width: 100%;
        }
    }
}
</style>