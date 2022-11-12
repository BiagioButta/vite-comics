<template>
  <div class="container debug">
    
    <div>
      <HeaderComponents/>
    </div>
    <div class="bg-black">
      <MainContents/>
    </div>
    <div class="bg-azure">
      <AzureComponents/>
    </div>
    <div class="bg-grey">
      <FooterComponents/>
    </div>

  </div>
</template>

<script>

  import HeaderComponents from './components/HeaderComponents.vue';
  import MainContents from './components/MainContents.vue';
  import AzureComponents from './components/AzureComponents.vue';
  import FooterComponents from './components/FooterComponents.vue';

  export default {
    components: {
      HeaderComponents,
      MainContents,
      AzureComponents,
      FooterComponents
    }
  }
</script>

<style lang="scss" scoped>

  .container{
    max-width: 1440px;
    margin: 0 auto;
    margin-top: 10px;
  }

  .bg-azure{
    background-color: #0282F9;
  }

  .bg-black{
    background-color: #1C1C1C;
  }

 



</style>