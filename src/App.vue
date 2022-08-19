<template lang='pug'>
div
  HeaderComponent
  main.container
    ul.product__list 
      ProductItem(
                  v-for="product in productList",
                  :img ="product.img",
                  :content ="product.content"
              )

</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import ProductItem from './components/ProductItem.vue';


export default {
  name: 'App',
  components: {
    HeaderComponent,
    ProductItem
},
   data (){
        return {
            }
            },
}
</script>

<style lang="scss">
    @import "./assets/scss/general.scss";


#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

</style>
