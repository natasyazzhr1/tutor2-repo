<template>
  <div class="container">
    <input v-model="input" type="text">
    <Card v-for="(post, index) in posts" :key="index" :post="post" />
  </div>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
  name: 'Home',
  components: {
    Card,
  },
  data() {
    return {
      posts: [
        {
          judul: 'Ini vue dan nuxt 1',
          caption: 'GEP oke banget',
          likes: 0,
          input: ''
        },
        {
          judul: 'Ini vue dan nuxt 2',
          caption: 'GEP oke banget',
          likes: 0,
          input: ''
        },
        {
          judul: 'Ini vue dan nuxt 3',
          caption: 'GEP oke banget',
          likes: 0,
          input: ''
        },
        {
          judul: 'Ini vue dan nuxt 4',
          caption: 'GEP oke banget',
          likes: 0,
          input: ''
        },
        {
          judul: 'Ini vue dan nuxt 5',
          caption: 'GEP oke banget',
          likes: 0,
          input: ''
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.hijau {
  color: red;
}
.merah {
  color: green;
}
</style>
