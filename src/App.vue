<template>
  <div class="container">
    
  <div>
    <HeaderComponents/>
  </div>
  <div>
    <MainContents/>
  </div>
  <div>
    <AzureComponents/>
  </div>
  <div>
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
    width: 100%;
  }


</style>