<template>
  <Header/>
  <div class="container">
    <h1>Категории</h1>
      <div class="cards">
        <template v-for="tag in tags">
          <Card :tag="tag"/>
        </template>
      </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import Card from '@/components/Card.vue';
import Header from '@/components/Header.vue';
import axios from 'axios'

onMounted(async() => {
  await getData()
})

const tags = ref([])

const getData = async() => {
  await axios.get('https://nlstar.com/ru/api/catalog3/v1/menutags/', {
    params: {
      city_id: 1
    }
  })
  .then(function (response) {
    console.log(response.data);
    tags.value = response.data.tags
  })
  .catch(function (error) {
    console.log(error);
  })
}

</script>

<style scoped>
.container {
  width: 1150px;
  margin: 0 auto;
}
h1 {
  margin-top: 20px;
}
.cards {
  margin-top: 20px;
  display: flex;
  gap: 22px;
  flex-wrap: wrap;
}
</style>