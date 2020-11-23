<template>
  <div>
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
      input: '',
      posts: [
        {
          judul: 'Ini vue dan nuxt 1',
          caption: 'GEP oke banget',
          likes: 0,
        },
        {
          judul: 'Ini vue dan nuxt 2',
          caption: 'GEP oke banget',
          likes: 0,
        },
        {
          judul: 'Ini vue dan nuxt 3',
          caption: 'GEP oke banget',
          likes: 0,
        },
        {
          judul: 'Ini vue dan nuxt 4',
          caption: 'GEP oke banget',
          likes: 0,
        },
        {
          judul: 'Ini vue dan nuxt 5',
          caption: 'GEP oke banget',
          likes: 0,
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
input {
  border: 1px solid #333333;
  border-radius: 10px;
  padding: 0 5px;
  outline: none;
}
</style>
