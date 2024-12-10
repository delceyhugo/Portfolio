<script setup>
import Button from './base/Button.vue';

const redirect = (url) => {
    window.open(url, '_blank').focus();
}
</script>


<template>
    <section id="Contact">
        <article class="anim-from-left">
            <h1>Un message suffit</h1>
            <p>
                Un projet en tête, une question qui brûle ou juste envie de discuter ?<br>
                Je suis à un clic de souris !<br>
                Et toujours curieux de découvrir de nouveaux défis et opportunités !<br>
                Un petit mot dans le formulaire, ou un email si vous préférez !<br>
            </p>
            <aside>
                <h2>Mon e-mail:</h2>
                <a href="mailto:delcey.hugo@outlook.fr">delcey.hugo@outlook.fr</a>
            </aside>
            <aside>
                <h2>
                    Ou retrouvez-moi sur :
                </h2>
                <div>
                    <img @click="redirect('https://github.com/delceyhugo')" width="40" height="40" src="@/assets/icon/github.png" alt="github"/>
                    <img @click="redirect('https://www.linkedin.com/in/hugo-delcey-240bb4174/')" width="40" height="40" src="@/assets/icon/linkedin.png" alt="linkedin"/>
                    <img @click="redirect('https://x.com/DelceyHugo')" width="40" height="40" src="@/assets/icon/x.png" alt="twitterx"/>
                </div>
            </aside>
        </article>
        <form class="anim-from-right" action="https://api.web3forms.com/submit" method="POST">
            <input type="hidden" name="access_key" value="56306e44-e705-4d34-91d0-b7e89556208b">
            <input type="checkbox" name="botcheck" class="hidden" style="display: none;">
            <div>
                <input type="name" name="name" placeholder="Qui est-tu ?" required>
                <input type="email" name="email" placeholder="Votre mail ici" required>
            </div>
            <textarea name="message" placeholder="Dites-m'en plus" required></textarea>
            <Button type="submit">C’est parti !</Button>
        </form>
    </section>

</template>


<style lang='scss' scoped>

section{
    // Layout
    display: flex;
    flex-direction: row;
    gap: 10px;
    padding: 10px;
    flex-wrap: wrap;
    article{
        display: flex;
        flex-direction: column;
        gap: 30px;
        min-width: 400px;
        flex: 1;
        aside{
            display: flex;
            flex-direction: column;
            h2{
                opacity: 1;
                color: rgba(0, 0, 0, 0.6);
                font-size: 20px;
                font-weight: var(--font-regular);
                line-height: 28px;
            }
            a{
                color: var(--color-dark);
            }
            div{
                display: flex;
                flex-direction: row;
                gap: 5px;
                img{
                    cursor: pointer;
                    transition: all 0.15s ease-in-out;
                    &:hover{
                        transform: scale(1.1);
                    }
                }
            }

        }

    }
    form{
        display: flex;
        flex-direction: column;
        flex: 1;
        gap: 30px;
        align-items: flex-end;
        min-width: 400px;
        div{
            display: flex;
            flex-direction: row;
            gap: 30px;
            width: 100%;
        }
        input, textarea{
            // Layout
            width: 100%;
            height: 60px;
            padding: 0px 20px;
            // Style
            border: 2px solid var(--color-black);
            border-radius: 12px;
            box-shadow: 4px 4px 0px var(--color-black);
            outline: none;
            transition: all 0.15s ease-in-out;
            // Font
            font-family: var(--font-grotesk);
            font-weight: var(--font-regular);
            font-size: 18px;
            color: var(--color-dark);
            &:focus{
                box-shadow: 0px 0px 0px var(--color-black);
                transform: translate(4px, 4px);
            }
            &::placeholder{  
                color: rgba(0, 0, 0, 0.5);
            }
        }
        textarea{
            flex: 1;
            padding: 20px 20px;
            min-height: 200px;
        }
    }
}

</style>