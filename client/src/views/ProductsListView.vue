<template>
  <div class="container mt-4">
    <div class="d-flex justify-content-between align-items-center mb-3">
      <h2>Liste des produits</h2>
      <router-link to="/new-product" class="btn btn-success">Créer</router-link>
    </div>

    <table class="table table-hover">
      <thead>
        <tr>
          <th>Nom</th>
          <th>Description</th>
          <th>Prix</th>
          <th>Actions</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="product in products" :key="product.id" @click="navigateToProduct(product.id)" class="table-row-clickable">
          <td>{{ product.name }}</td>
          <td>{{ product.description }}</td>
          <td>{{ product.price }}</td>
          <td>
            <a class="btn btn-primary btn-sm me-2" @click.stop.prevent="navigateToEditProduct(product.id)">Mettre à jour</a>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    name: "ProductListView",
    props: {
      products: {
        type: Array,
        required: true,
      },
    },
    methods: {
      navigateToProduct(id) {
        this.$router.push(`/product/${id}`);
      },
      navigateToEditProduct(id){
        this.$router.push(`/edit-product/${id}`);
      }
    },
  };
</script>

<style scoped></style>
