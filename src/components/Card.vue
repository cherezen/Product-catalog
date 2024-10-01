<template>
  <div class="card" :style="{backgroundImage: `url(${tag.image})`}">
    <p class="card__name" :style="{color: tag.text_color}">{{ tag.name }}</p>
  </div>
</template>

<script setup>
const props = defineProps(['tag'])
</script>

<style scoped>
.card {
  width: 271px;
  height: 152px;
  background-position: center center;
  padding: 20px;
  font-size: 24px;
  line-height: 28px;
}
</style>