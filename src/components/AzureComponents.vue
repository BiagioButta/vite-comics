<template>
    <div class="w70pc">
        <div class="h-align-center">
            <ul>
                <li v-for="(icon,index) in icons" :key="index"><a :href="icon.url"><img :src="getImagePath(`${icon.img}`)" alt="">  {{icon.link}}</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AzureComponents',
        data(){
            return{
                icons: [
                    {
                        img: '../assets/img/buy-comics-digital-comics.png',
                        link: 'Digital Comics',
                        url: '#'
                    },
                    {
                        img: '../assets/img/buy-comics-merchandise.png',
                        link: 'DC Merchandise',
                        url: '#'
                    },
                    {
                        img: '../assets/img/buy-comics-subscriptions.png',
                        link: 'subscription',
                        url: '#'
                    },
                    {
                        img: '../assets/img/buy-comics-shop-locator.png',
                        link: 'comics shop locator',
                        url: '#'
                    },
                    {
                        img: '../assets/img/buy-dc-power-visa.svg',
                        link: 'Dc power Visa',
                        url: '#'
                    }
                ]
            }
        },
        methods: {
            getImagePath: function(imgPath) {
                return new URL(imgPath, import.meta.url).href;
            }
        }
    }
</script>

<style lang="scss" scoped>

    ul{
        display: flex;

        li{
            a{
                display: flex;
                align-items: center;
                color: white;
                font-size: 1rem;
                text-transform: uppercase;
                margin: 0 10px;
            }
        }
    }

    img{
        width: 50px;
        height: 70px;
    }

    .h-align-center{
        height: 150px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    

</style>