<template>
    <div>
        <div>
        <ul>
        <li v-for="(icon,index) in icons"> <img src="${{icon.img}}" alt="">  {{icon.link}}</li>
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
                        link: 'Digital Comics'
                    },
                    {
                        img: '../assets/img/buy-comics-merchandise.png',
                        link: 'DC Merchandise'
                    },
                    {
                        img: '../assets/img/buy-comics-subscriptions.png',
                        link: 'subscription'
                    },
                    {
                        img: '../assets/img/buy-comics-shop-locator.png',
                        link: 'comics shop locator'
                    },
                    {
                        img: '../assets/img/buy-dc-power-visa.svg',
                        link: 'Dc power Visa'
                    }
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
        background-color: #0282F9;
        width: 100%;
        height: 200px;
    }

    ul{
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: center;

        li{
            list-style: none;
            text-transform: uppercase;
            color: white;
        }
    }

    

</style>