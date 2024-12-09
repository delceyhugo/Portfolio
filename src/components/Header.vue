<script setup>

</script>


<template>
    <nav>
        <aside>
            <img src="@/assets/logo.svg" alt="Logo">
            <h1>hugo.delcey</h1>
        </aside>
        <ul>
            <span></span>
            <li>
                <a href="#">Qui suis-je</a>
            </li>
            <span></span>
            <li>
                <a href="#">Portfolio</a>
            </li>
            <span></span>
            <li>
                <a href="#">Contact</a>
            </li>
            <span></span>
            <li>
                <a href="#">CV</a>
            </li>
            <span class="last"></span>
            <li>
                <a href="#">
                    <img src="@/assets/Menu.png" alt="menu">
                </a>
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
        }
    }
    ul{
        display: flex;
        flex-direction: row;
        >span{
            position: relative;
            // top: 0;
            // left: 0;
            width: 2px;
            height: 100%;
            background-color: var(--color-black);
            &.last{
                display: none;
            }
            
        }

        li{
            list-style: none;
            padding: 0px 20px;
            display: flex;
            align-items: center;
            position: relative;
            cursor: pointer;
            transition: all 0.15s ease-in-out;
            border: 2px solid transparent;
            &:hover{
                background-color: var(--color-yellow);
                box-shadow: 4px 4px 0px var(--color-black);
                transform: translate(-4px, -4px);
                border: 2px solid var(--color-black);
                
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
            &:nth-child(8){
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