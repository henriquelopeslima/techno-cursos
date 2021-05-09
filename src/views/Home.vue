<template>
  <div>
      <div v-if="api">
    <h1>Home</h1>
        <p>{{ api }}</p>
      </div>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "home",
  components: {},
  mixins: [fetchData],
  created() {
    this.fetchData(this.$options.name);
    console.log(this);
  },
};
</script>
