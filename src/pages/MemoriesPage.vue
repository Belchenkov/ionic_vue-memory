<template>
  <base-layout page-title="All Memories">
    <memories-list :memories="memories" />
  </base-layout>
</template>

<script>
import MemoriesList from "../compoents/memories/MemoriesList";

export default {
  name: "MemoriesPage",
  components: {
    MemoriesList
  },
  data() {
    return {}
  },
  computed: {
    memories() {
      return this.$store.getters.memories;
    }
  }
}
</script>

<style scoped>

</style>