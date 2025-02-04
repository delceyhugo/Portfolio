<script setup>
import { ref } from 'vue';

const menu = ref(false)



</script>


<template>
    <nav class="anim-from-top">
        <aside>
            <img src="@/assets/logo.svg" alt="Logo">
            <h1>hugo.delcey</h1>
        </aside>
        <ul>
            <li>
                <a href="#Overview">Qui suis-je</a>
                <span></span>
            </li>
            <li>
                <a href="#Highlight">Portfolio</a>
                <span></span>
            </li>
            <li>
                <a href="#Contact">Contact</a>
                <span></span>
            </li>
            <li>
                <a target="_blank" href="https://drive.google.com/file/d/1R2Ft0VzkxHfNieBKRraDqUOQOPuseMEL/view?usp=sharing">CV</a>
                <span></span>
            </li>
            <li @click="menu = !menu">
                <button >
                    <img src="@/assets/icon/menu.png" alt="menu">
                    <ul v-if="menu">
                        <li>
                            <a href="#Overview">
                                <img src="@/assets/icon/me.png" alt="Qui suis-je">
                            </a>
                        </li>
                        <li>
                            <a href="#Highlight">
                                <img src="@/assets/icon/portfolio.png" alt="Portfolio">
                            </a>
                        </li>
                        <li>
                            <a href="#Contact">
                                <img src="@/assets/icon/contact.png" alt="Contact">
                            </a>
                        </li>
                        <li>
                            <a href="">
                                <img src="@/assets/icon/cv.png" alt="CV">
                            </a>
                        </li>
                    </ul>
                </button>
                <span class="last"></span>
            </li>
        </ul>
    </nav>
</template>


<style lang='scss' scoped>
nav{
    display: flex;
    border: 2px solid var(--color-black);
    border-radius: 12px;
    box-shadow: 4px 4px 0px var(--color-black);
    // overflow: hidden;
    aside{
        display: flex;
        flex: 1;
        flex-direction: row;
        align-items: center;
        gap: 14px;
        padding: 5px 30px;
        img{
            width: 29px;
            height: auto;
        }
        h1{
            font-family: var(--font-grotesk);
            font-size: 29px;
            font-weight: var(--font-bold);
            color: var(--color-dark);
            @media screen and (max-width: 440px) {
            font-size: 20px;
            }
        }
    }
    ul{
        display: flex;
        flex-direction: row;
        li{
            list-style: none;
            padding: 0px 20px;
            display: flex;
            align-items: center;
            position: relative;
            cursor: pointer;
            transition: all 0.15s ease-in-out;
            border: 2px solid transparent;
            >span{
                position: absolute;
                top: -2px;
                left: -2px;
                width: 2px;
                height: calc(100% + 4px);
                background-color: var(--color-black);
                transition: all 0.15s ease-in-out;
                &.last{
                    display: none;
                }
            }
            &:hover{
                background-color: var(--color-yellow);
                box-shadow: 4px 4px 0px var(--color-black);
                transform: translate(-4px, -4px);
                border: 2px solid var(--color-black);
                >span{
                    background-color: transparent;
                }
            }
            &:active{
                background-color: var(--color-yellow);
                box-shadow: 0px 0px 0px var(--color-black);
                border: 2px solid transparent;
                
                transform: translate(0px, 0px);
            }
            a{
                font-family: var(--font-grotesk);
                font-size: 29px;
                font-weight: var(--font-bold);
                color: var(--color-dark);
            }
            &:nth-child(4){
                border-radius: 0px 9px 9px 0px;
            }
            &:last-child{
                display: none;
                border-radius: 0px 9px 9px 0px;
            }
        }
    }
    @media screen and (max-width: 1200px) {
        ul{
            li{
                display: none;
                &:last-child{
                    display: flex;





                    button{
                        background-color: transparent;
                        border: none;
                        cursor: pointer;
                        img{
                            width: 40px;
                            height: 40px;
                        }



                        ul{
                            position: absolute;
                            top: 110%;
                            left: 0px;
                            display: flex;
                            flex-direction: column;
                            gap: 0px;
                            padding: 0px;
                            border: 2px solid var(--color-black);
                            border-radius: 12px 12px 12px 12px;
                            box-shadow: 4px 4px 0px var(--color-black);
                            background-color: var(--color-white);
                            transition: all 0.15s ease-in-out;
                            li{
                                display: flex;
                                flex-direction: column;
                                align-items: flex-start;
                                gap: 0px;
                                padding: 10px 20px;
                                border: none;
                                border-radius: 0px;
                                box-shadow: none;
                                background-color: transparent;
                                transition: all 0.15s ease-in-out;
                                a{
                                    font-family: var(--font-grotesk);
                                    font-size: 29px;
                                }
                            }
                        }
                    }
                }
            }
            >span{
                display: none;
                &.last{
                    display: flex;
                }
            }
        }
        
    }
}

</style>