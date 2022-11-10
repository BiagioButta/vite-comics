<template>
    <div class="w70pc">
        <div class="bg-img"></div>
        <div class="social">
            <button>Sign Up now!</button>
            <div>
                <span>Follow us</span>
                <ul><li v-for="(social,index) in socialIcons" :key="index"><a :href="social.url"><img :src="getImagePath(`${social.img}`)" alt=""></a></li></ul>
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
                    {
                        img: '../assets/img/footer-facebook.png',
                        url: '#'
                    },
                    {
                        img: '../assets/img/footer-twitter.png',
                        url: '#'
                    },
                    {
                        img: '../assets/img/footer-youtube.png',
                        url: '#'
                    },
                    {
                        img: '../assets/img/footer-periscope.png',
                        url: '#'
                    },
                    {
                        img: '../assets/img/footer-pinterest.png',
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

   img{
    width: 50px;
   }

</style>