<template>
    <div class="w70pc row">
        <div class="col">

            <img src="../assets/img/dc-logo.png" alt="">

        </div>
        <div class="col align-center">
        
            <ul>
                <li v-for="(link,index) in linkNav"><a href="#">{{link}}</a></li>
            </ul>
        
        </div>

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

   

    ul{ display: flex;

        li{
            margin-left: 10px;
            font-size: 1rem;
            text-transform: uppercase;
        }
    }

    .align-center{
        display: flex;
        align-items: center;
    }
    
    img{
        vertical-align: middle;
    }




</style>