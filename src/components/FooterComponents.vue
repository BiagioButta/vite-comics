<template>
    <div class="bg-img">
    
        <div class="w70pc">
            
            <div class="row color-white justify-between">
                
                <div class="col-1">
                    <ul><bold>DC</bold>
                        <li v-for="(item,index) in linkFooterDcComics" :key="index"><a href="">{{item}}</a></li>
                    </ul>
                    <ul><bold>DC</bold>
                        <li v-for="(item,index) in linkFooterShop" :key="index"><a href="">{{item}}</a></li>
                    </ul>
                </div>
                <div class="col-1">
                    <ul><bold>DC</bold>
                        <li v-for="(item,index) in linkFooterDc" :key="index"><a href="">{{item}}</a></li>
                    </ul>
                </div>
                <div class="col-1">
                    <ul><bold>DC</bold>
                        <li v-for="(item,index) in linkFooterSites" :key="index"><a href="">{{item}}</a></li>
                    </ul>
                </div>

                <div class="col-7">
                </div>

            </div>
            
        </div>

    </div>

    <div class="bg-grey">

        <div class="w70pc">
            
            <div class="social d-flex justify-between align-center">
                    <button>Sign Up now!</button>

                    <div class="d-flex align-center">
                        <span><bold>Follow us</bold></span>
                        <ul class="d-flex"><li v-for="(social,index) in socialIcons" :key="index"><a :href="social.url"><img :src="getImagePath(`${social.img}`)" alt=""></a></li></ul>
                    </div>
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
                  
                ],
                linkFooterDcComics: [ 'Characters', 'Comics', 'Movies', 'Tv', 'Games', 'Videos', 'News' ],
                linkFooterShop: [ 'Shop', 'Shop' ],
                linkFooterDc: [ 'Terms of Use', 'Terms of Use', 'Terms of Use', 'Terms of Use', 'Terms of Use', 'Terms of Use', 'Terms of Use', 'Terms of Use', 'Terms of Use', 'Terms of Use'],
                linkFooterSites: [ 'DC', 'DC', 'DC', 'DC', 'DC', 'DC']
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

    .bg-img{
        background-image: url(../assets/img/footer-bg.jpg);
        height: 420px;
    }

   img{
    width: 50px;
   }

   .w70pc{
    height: 100%;
   }

   span{
    color:  #0282F9;
    margin-right: 10px;
    text-transform: uppercase;
   }

   button{
    background-color: transparent;
    border-color: #0282F9;
    color: white;
    text-transform: uppercase;
    padding: 5px 2px;
   }

   .bg-grey{
    background-color: #303030;
  }

  .color-white{
    color: white;
  }

  ul{
    margin-top: 20px;
  }

  .col-7{
    background-image: url(../assets/img/dc-logo-bg.png);
    background-size: cover;
  }

  a{
    color: white;
  }


</style>