<template>
  <div>
    <h1>父组件</h1>
    <children :count="count" @passMyCount="getCount"></children>
    <button @click="logCount">展示接受到的子值</button>
    <brother></brother>
  </div>
</template>

<script>
import children from "@/components/children";
import brother from "@/components/brother";
export default {
  components: {
    children,brother
  },
  data() {
    return {
      count: 1,
      sonCount: null
    }
  },
  methods: {
    getCount(e) {
      console.log(e);
      this.sonCount = e
    },
    logCount() {
      console.log(this.sonCount)
    }
  }
}
</script>

<style scoped>

</style>