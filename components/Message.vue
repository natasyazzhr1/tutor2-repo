<template>
  <div class="coklat">
    <div>
      {{ coklatKapital }}
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Message',
    props: {
      coklat: {
        type: String,
        default: ''
      },
    },
    computed: {
      coklatKapital() {
        let coklat = this.coklat
        let newcoklat = coklat.toUpperCase()
        return newcoklat
      }
    },
  }
</script>

<style lang="scss" scoped>
.coklat {
  width: 100px;
  height: 100px;
  margin: 10px;
  padding: 5px;
  border-radius: 20px;
  background-color: #333333;
  color: white;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: background-color 0.3s ease-in-out;
  &:hover {
    background-color: #33333360;
    cursor: pointer;
  }
}
</style>