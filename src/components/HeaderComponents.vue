<template>
    <div>
        <img src="../assets/img/dc-logo.png" alt="">

        <ul>
        <li v-for="(link,index) in linkNav"><a href="#">{{link}}</a></li>
        </ul>
    </div>

</template>

<script>
import { toValidAssetId } from '@vue/compiler-core';

    export default {
        name: 'HeaderComponents',
        data(){
            return{
                linkNav: [
                    'Characters',
                    'Comincs',
                    'Movies',
                    'Tv',
                    'Games',
                    'Collectibles',
                    'Videos',
                    'Fans',
                    'News',
                    'Shop'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

*{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    div{
        background-color: white;
        width: 70%;
        height: 110px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    ul{
        display: flex;

        li{
            list-style: none;
            
            a{
                text-decoration: none;
                text-transform: uppercase;
                font-size: 1.5rem;
                margin-left: 50px;
                color: black;
                cursor: pointer;
            }
        }
    }

</style>