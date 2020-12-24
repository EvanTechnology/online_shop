<template>
  <div class="mainWrapper">
        <Catalog />
        <Cart />
  </div>

</template>

<script>
import Catalog from "./catalog"
import Cart from "./cart"
export default {
    name: "mainWrapper",
    components: {
        Catalog, Cart
    },
    props: {},
    data() {
        return {
            title: "Main Wrapper"
        }
    },
    computed: {},
    methods: {},
    watch: {},
    mounted() {}
}
</script>

<style lang="scss" scoped>
    .mainWrapper {
        max-width: 900px;
        margin: 0 auto;
    }
</style>
