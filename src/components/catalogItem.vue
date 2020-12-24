<template>
  <div class="catalogItem">
      <img class="catalog-item__img" 
      :src="require('../assets/images/'+product_data.image)" 
      alt="img">
      <p class="catalog-item__name">{{product_data.name}}</p>
      <p class="catalog-item__price">price: ${{product_data.price}}</p>
      <button 
      class="btn catalog-item__add-to-cart-btn" 
      type="submit"
      @click.prevent="submitHandler"
      >
      Add to cart
      </button>
  </div>
</template>

<script>
export default {
    name: "catalogItem",
    components: {},
    props: {
        product_data: {
            type: Object,
            default() {
                return {}
            }
        }
    },
    data() {
        return {
        }
    },
    computed: {},
    methods: {
        submitHandler() {
            this.$emit("sendBarcode", this.product_data.barcode)
        }
    },
    watch: {},
    mounted() {}
}
</script>

<style lang="scss">
    .catalogItem {
        flex-basis: 25%;
        box-shadow: 0 0 8px 0 #e0e0e0;
        padding: 8px ;
        margin-bottom: 8px;
    };
    .catalog-item__img {
        width: 150px;
        height: 300px;
        object-fit: cover;
    }
</style>