<template>
    <div>
        <div class="bg-img"></div>
        <div class="social">
            <button>Sign Up now!</button>
            <div>
                <span>Follow us</span>
                <ul><li v-for="(social,index) in socialIcons"> <img src="${{social}}" alt=""></li></ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterComponents',
        data() {
            return {
                socialIcons: [
                    '../assets/img/footer-facebook.png',
                    '../assets/img/footer-twitter.png',
                    '../assets/img/footer-youtube.png',
                    '../assets/img/footer-periscope.png',
                    '../assets/img/footer-pinterest.png'
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>

    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    div{
        width: 100%;
        height: 500px;
        background-color: #303030;
    }

    .bg-img{
        background-image: url(../assets/img/footer-bg.jpg);
    }

    button{
        background-color: transparent;
        border-color: #0282F9;
        text-transform: uppercase;
        color: white;
    }

    span{
        color: #0282F9;
        text-transform: uppercase;
    }



</style>