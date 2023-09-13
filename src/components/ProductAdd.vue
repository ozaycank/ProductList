<template>
  <div id="addForm">
    <form @submit.prevent="handleAdd">
      <div class="form-group">
        <label for="id">Id</label>
        <input v-model="product.id" type="text" class="form-control" id="id" />
      </div>
      <div class="form-group">
        <label for="categoryId">Category</label>
        <input
          v-model="product.categoryId"
          type="text"
          class="form-control"
          id="categoryId"
        />
      </div>
      <div class="form-group">
        <label for="categoryId">Product Name</label>
        <input
          v-model="product.productName"
          type="text"
          class="form-control"
          id="productName"
        />
      </div>
      <div class="form-group">
        <label for="categoryId">Description</label>
        <input
          v-model="product.Description"
          type="text"
          class="form-control"
          id="Description"
        />
      </div>
      <div class="form-group">
        <label for="categoryId">unitPrice</label>
        <input
          v-model="product.unitPrice"
          type="text"
          class="form-control"
          id="unitPrice"
        />
      </div>
      <div class="form-group">
        <label for="categoryId">unitsInStock</label>
        <input
          v-model="product.unitsInStock"
          type="text"
          class="form-control"
          id="unitsInStock"
        />
      </div>
      <button type="submit" class="btn btn-sm btn-success">Add</button>
    </form>
  </div>
</template>
<script>
export default {
  name: "product-add",
  data() {
    return {
      product: {
        id: "",
        categoryId: "",
        productName: "",
        Description:"",
        unitPrice: "",
        unitInStock: "",
      },
    };   
  },
  methods:{
        handleAdd(){
            this.$emit("add:product",this.product)
        }
    }
};
</script>
<style scoped>
#addForm{
    margin:100px
}
</style>