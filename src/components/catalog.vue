<template>
  <div class="catalog">
      <h1>Catalog</h1>
      <div class="catalog__list">
          <CatalogItem 
            v-for="product in products"
            :key="product.barcode"
            :product_data="product"
            @sendBarcode="showBarcode"
          />
      </div>
  </div>
</template>

<script>
import CatalogItem from "./catalogItem"
export default {
    name: "catalog",
    components: {
        CatalogItem
    },
    props: {},
    data() {
        return {
             products: [
                { image: "1.jpg",
                    name: "T-shirt",
                    price: 25,
                    barcode: "t1",
                    available: true
                },
                { image: "2.jpg",
                    name: "T-shirt",
                    price: 35,
                    barcode: "t2",
                    available: true
                }
    ]
        }
    },
    computed: {},
    methods: {
        showBarcode(data) {
            console.log(data)
        }
    },
    watch: {},
    mounted() {}
}
</script>

<style lang="scss">
    .catalog {
        &__list {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }
    }
</style>