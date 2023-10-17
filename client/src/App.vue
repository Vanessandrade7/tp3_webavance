<template>
  <div>
    <!-- Navigation-->
    <navbar />
    <router-view :products="products" :addInv="addInventory" :removeInv="removeInventory" :remove="removeItem" :updateInv="updateInventory" />
  </div>
</template>

<script>
  import ProductDataService from "@/services/ProductDataService";
  import Navbar from "./components/Navbar.vue";
  export default {
    components: {
      Navbar,
    },
    data() {
      return {
        products: [],
      };
    },
    watch: {
        $route: {
            immediate: true,
            handler(to) {
                document.title = to.meta.title || 'Product List';
            }
        },
    },
    methods: {
      addInventory(data) {
        this.products.push(data);
      },
      removeInventory(id) {
        this.products.splice(this.products.findIndex(p=> p.id === id), 1);
      },
      updateInventory(id, data) {
        const product = this.products.find(p=> p.id == id);
        product.name = data.name;
        product.photo = data.photo;
        product.price = data.price;
        product.description = data.description;
        product.category = data.category;
      },
    },
    mounted() {
      ProductDataService.getAll().then((response) => {
        this.products = response.data;
      });
    },
  };
</script>
