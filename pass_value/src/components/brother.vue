<template>
  <div>
    <h2>子组件的兄弟组件</h2>
  </div>
</template>

<script>
export default {
  name: "brother",
  created() {
    this.$bus.$on('passBroCount', 'this.getBroCount')
  },
  methods: {
    getBroCount(e) {
      console.log(e + '兄弟组件传的值')
    }
  }
}
</script>

<style scoped>

</style>