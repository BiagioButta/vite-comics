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

    div{
        background-color: white;
        width: 70%;
        margin: 0 auto;
    }

</style>