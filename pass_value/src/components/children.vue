<template>
  <div class="children">
    <h2>子组件</h2>
    <span>父亲组件传过来的值{{count}}</span>
    <button @click="passMyCount">子传父值</button>
    <Grandson></Grandson>
  </div>
</template>

<script>
import Grandson from "@/components/Grandson";
export default {
  components: {
    Grandson
  },
  name: "children",
  props: ['count'],
  methods: {
    passMyCount() {
      this.$emit('passMyCount', 'myCount is 24');
      this.$bus.$emit('passBroCount','a age ');
    }
  }
}
</script>

<style scoped>
  .children {
    color: red;
  }
</style>