<template>
  <div>
      <div v-if="api">
    <h1>Cursos</h1>
        <p>{{ api }}</p>
      </div>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "cursos",
  components: {},
  mixins: [fetchData],
  created() {
    this.fetchData(this.$options.name);
  },
};
</script>
