<template>
    <div class="hero-img">
    </div>
    <div class="w70pc">
        <div class="row debug">

          <div class="col-1 debug">
          
            <div class="prev" @click="prev()"></div>
              
          </div>

          <div class="col-7 debug"><img :src="card[indexCard].thumb" alt="{{card[indecCard].series}}"></div>

          <div class="col-3 debug"><h1 class="mb">{{card[indexCard].series}}</h1><h3 class="mb">{{card[indexCard].price}}</h3><p>{{card[indexCard].type}}</p></div>

          <div class="col-1 debug">

            <div class="next" @click="next()"></div>

          </div>


            
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MainComponents',
        data() {
          return {
            indexCard: 0,
            card: [
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                "price": "$19.99",
                "series": "Action Comics",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                "price": "$3.99",
                "series": "American Vampire 1976",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                "price": "$16.99",
                "series": "Aquaman",
                "type": "graphic novel"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                "price": "$2.99",
                "series": "Batgirl",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                "price": "$3.99",
                "series": "Batman",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                "price": "$2.99",
                "series": "Batman Beyond",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                "price": "$3.99",
                "series": "Batman/Superman",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                "price": "$4.99",
                "series": "Batman/Superman Annual",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                "price": "$5.99",
                "series": "Batman: The Joker War Zone",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                "price": "$6.99",
                "series": "Batman: Three Jokers",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                "price": "$4.99",
                "series": "Batman: White Knight Presents: Harley Quinn",
                "type": "comic book"
              },
              {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel"
              }
            ]
          }
        },
        methods: {
          prev(){
            this.indexCard--
            if(this.indexCard < 0){
              this.indexCard = this.card.length - 1
            }
          },
          next(){
            this.indexCard++
            if(this.indexCard > this.card.length - 1){
              this.indexCard = 0
            }
          }
        }
    }
</script>

<style lang="scss" scoped>

    div{
        color: white;
    }

    .prev {
      width: 20px;
      height: 20px;
      border-top: 5px solid white;
      border-left: 5px solid white;
      transform: rotate(-45deg);
      cursor: pointer;
    }

    .next {
      width: 20px;
      height: 20px;
      border-top: 5px solid white;
      border-left: 5px solid white;
      transform: rotate(135deg);
      cursor: pointer;
    }

    img{
      width: 300px;
    }

    .col-1{
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .col-7{
      display: flex;
      justify-content: center;
    }

    .col-3{
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .mb{
      margin-bottom: 20px;
    }
  

</style>