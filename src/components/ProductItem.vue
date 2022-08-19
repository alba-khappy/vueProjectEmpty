<template lang='pug'>
li.product__item
    a(href="/").product__link
        img(:src="require(`../assets/${img}`)").product__img
        p.product__content {{content}}
</template>


<script>
export default {
  name: 'ProductItem',
  props: {
            img: {
                type: String,
                required: true,
            },
            content: {
                type: String,
                required: true,
            }
        },
}
</script>

<style lang="scss">

@import "../assets/scss/general.scss";

.product__item {
    width: 205px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 25px;
}

.product__link {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.product__img {
    width: auto;
    height: 210px;
    margin-bottom: 15px;
}

.product__content {
    text-align: center;
    font-size: 12px;
    font-style: italic;
    font-family: Arial, Helvetica, sans-serif;
    color: $grayTextColor;
}

</style>
