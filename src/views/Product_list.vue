<template>
    <div class ="container my-5">
        
        <table class="table table-hover">
  <thead class="table table-primary">
    <tr>
      <th>ID</th>
      <th>title</th>
      <th>description</th>
      <th>Category</th>
      <th>Price</th>
      <th>Image</th>
    </tr>
  </thead>

  <tbody>
    <tr v-for="item in products" :key="item.id">
      <td>{{ item.id }}</td>
      <td>{{ item.title }}</td>
      <td>{{ item.description }}</td>
      <td>{{ item.Category }}</td>
      <td>{{ item.Price }}</td>
      <td>{{ item.Image }}</td>
      <td>
      <img
            :src="item.images"
            width="100"
            class="card-img-top"
            alt="Product Image"
            style="object-fit: contain; width: 100%; height: 200px"
          />
      </td>
    </tr>
        
  </tbody>

</table>


    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const products = ref([])
const loading = ref(true)
const error = ref(null)

onMounted(async () => {
  try {
    const res = await fetch('https://dummyjson.com/products')
    const data = await res.json()
    products.value = data.products
  } catch (err) {
    error.value = 'โหลดข้อมูลไม่สำเร็จ'
  } finally {
    loading.value = false
  }
})
</script>