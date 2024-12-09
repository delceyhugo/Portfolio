<script setup>
import { ref } from 'vue';
import Labels from './base/Labels.vue';

const frontSkills = ref([
    {
        name: 'HTML',
        color: 'var(--color-blue)'
    },
    {
        name: 'CSS',
        color: 'var(--color-pink)'
    },
    {
        name: 'JavaScipt',
        color: 'var(--color-red)'
    },
    {
        name: 'jQuery',
        color: 'var(--color-blue)'
    },
    {
        name: 'Bootstrap',
        color: 'var(--color-teal)'
    },
    {
        name: 'Flexbox & Grid',
        color: 'var(--color-pink)'
    },
    {
        name: 'Sass',
        color: 'var(--color-pink)'
    },
    {
        name: 'Vue',
        color: 'var(--color-red)'
    },
    {
        name: 'React',
        color: 'var(--color-red)'
    },
    {
        name: 'SEO',
        color: 'var(--color-blue)'
    },
    {
        name: 'Responsive',
        color: 'var(--color-teal)'
    },
    {
        name: 'TypeScript',
        color: 'var(--color-blue)'
    },
    {
        name: 'Animation',
        color: 'var(--color-pink)'
    },
    {
        name: 'Figma',
        color: 'var(--color-blue)'
    },
    {
        name: 'GSAP',
        color: 'var(--color-teal)'
    },
    {
        name: 'Photoshop',
        color: 'var(--color-blue)'
    },
    {
        name: 'Illustrator',
        color: 'var(--color-blue)'
    },
    {
        name: 'SVG',
        color: 'var(--color-pink)'
    },
    {
        name: 'Jasmine',
        color: 'var(--color-teal)'
    },
    {
        name: 'Three.js',
        color: 'var(--color-red)'
    }
])
const backSkills = ref([
    {
        name: 'Node',
        color: 'var(--color-teal)'
    },
    {
        name: 'Express',
        color: 'var(--color-pink)'
    },
    {
        name: 'PHP',
        color: 'var(--color-blue)'
    },
    {
        name: 'MongoDB',
        color: 'var(--color-red)'
    },
    {
        name: 'MySQL',
        color: 'var(--color-teal)'
    },
    {
        name: 'API REST',
        color: 'var(--color-red)'
    },
    {
        name: 'Socket.io',
        color: 'var(--color-blue)'
    },
    {
        name: 'phpMyAdmin',
        color: 'var(--color-red)'
    },
    {
        name: 'Postman',
        color: 'var(--color-pink)'
    },
    {
        name: 'npm',
        color: 'var(--color-blue)'
    },
    {
        name: 'Electron',
        color: 'var(--color-red)'
    },
    {
        name: 'FTP',
        color: 'var(--color-blue)'
    }
])
const otherSkills = ref([
    {
        name: 'CMS',
        color: 'var(--color-pink)'
    },
    {
        name: 'Wordpress',
        color: 'var(--color-blue)'
    },
    {
        name: 'Modélisation 3D',
        color: 'var(--color-teal)'
    },
    {
        name: 'Motion design',
        color: 'var(--color-blue)'
    },
    {
        name: 'Unreal Engine',
        color: 'var(--color-red)'
    },
    {
        name: 'After Effects',
        color: 'var(--color-teal)'
    },
    {
        name: 'UML',
        color: 'var(--color-pink)'
    },
    {
        name: 'Github',
        color: 'var(--color-blue)'
    },
    {
        name: 'Trello',
        color: 'var(--color-pink)'
    },
    {
        name: 'Figma',
        color: 'var(--color-red)'
    }
])
</script>


<template>
    <section>
        <h1>
            Les compétences qui me définissent
        </h1>
        <main>
            <section>
                <h2>Faire briller l’interface</h2>
                <div>
                    <Labels v-for="skill in frontSkills" :color="skill.color">
                        {{ skill.name }}
                    </Labels>
                </div>
            </section>
            <section>
                <h2>L’invisible mais essentiel</h2>
                <div>
                    <Labels v-for="skill in backSkills" :color="skill.color">
                        {{ skill.name }}
                    </Labels>
                </div>
            </section>
            <section>
                <h2>Au-delà du code</h2>
                <div>
                    <Labels v-for="skill in otherSkills" :color="skill.color">
                        {{ skill.name }}
                    </Labels>
                </div>
            </section>
            <section id="softSkills">
                <h2>Au-delà des compétences techniques</h2>
                <article>
                    <div>
                        <Labels>Curieux</Labels>
                        <p>D’une nature curieuse, j’aime plonger dans les rouages de ce qui m’entoure.</p>
                    </div>
                    <div>
                        <Labels>Autonome</Labels>
                        <p>Je tire mon autonomie de mon parcours autodidacte, où apprendre seul est une force.</p>
                    </div>
                    <div>
                        <Labels>Dévoué</Labels>
                        <p>Fiabilité et confiance sont au cœur de ma manière de travailler.</p>
                    </div>
                </article>
            </section>
        </main>
    </section>

</template>


<style lang='scss' scoped>
section{
    display: flex;
    flex-direction: column;
    gap: 35px;
    h1{
        text-align: center;
    }
    main{
        display: flex;
        flex-direction: column;
        gap: 25px;
        section{
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            div{
                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: center;
                gap: 10px;
                flex-wrap: wrap;
            }
            &#softSkills{
                display: flex;
                flex-direction: column;
                gap: 10px;
                align-items: center;
                article{
                    display: flex;
                    flex-direction: column;
                    gap: 10px;
                    div{
                        display: flex;
                        flex-direction: row;
                        justify-content: flex-start;
                        gap: 10px;
                        p{
                            font-family: var(--font-mono);
                            font-weight: var(--font-regular);
                            font-size: 16px;
                            line-height: normal;
                        }
                    }
                }
            }
        }
    }
}

</style>