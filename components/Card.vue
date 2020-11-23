<template>
  <div class="card-container">
    <transition name="fade">
      <h1 :class="checkLikes()">
        {{ post.judul }}
      </h1>
    </transition>
    <p>{{ post.caption }}</p>
    <span>{{ post.likes }}</span>
    <v-btn class="pink white--text" flat @click="post.likes++">
      Click Me!
    </v-btn>
  </div>
</template>

<script>
  export default {
    name: 'Card',
    props: {
      post: {
        type: Object,
        default: () => {}
      },
    },
    methods: {
    checkLikes() {
      if (this.post.likes > 10) {
        return 'hijau'
      } else {
        return 'merah'
      }
    }
  },
}
</script>

<style lang="scss" scoped>
.card-container {
  background-color: #333333;
  border-radius: 20px;
  padding: 10px;
  margin: 10px;
  font-family: 'Montserrat';
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  transition: background-color 0.3s ease-in-out;
  &:hover {
    cursor: pointer;
    background-color: #33333342;
  }
  @media only screen and (max-width: 600px) {
    display: none;
  }
  .hijau {
    color: green;
  }
  .merah {
    color: red;
  }
}
    
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.v-btn {
  font-family: 'Consolas';
  background-color: pink;
}
</style>