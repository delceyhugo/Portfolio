<script setup>

</script>


<template>
    <nav>
        <aside>
            <img src="@/assets/logo.svg" alt="Logo">
            <h1>hugo.delcey</h1>
        </aside>
        <ul>
            <li>
                <a href="#">Qui suis-je</a>
                <span></span>
            </li>
            <li>
                <a href="#">Portfolio</a>
                <span></span>
            </li>
            <li>
                <a href="#">Contact</a>
                <span></span>
            </li>
            <li>
                <a href="#">CV</a>
                <span></span>
            </li>
            <li>
                <a href="#">
                    <img src="@/assets/icon/menu.png" alt="menu">
                </a>
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