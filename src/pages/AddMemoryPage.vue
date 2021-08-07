<template>
  <base-layout
      page-title="Add a Memory"
      page-default-back-link="/memories"
  >
    <create-memory-form @save-memory="saveMemory"></create-memory-form>
  </base-layout>
</template>

<script>
import CreateMemoryForm from "../compoents/memories/CreateMemoryForm";

export default {
  name: "AddMemoryPage",
  components: {
    CreateMemoryForm
  },
  methods: {
    saveMemory(memoryData) {
      this.$store.dispatch('addMemory', memoryData);
      this.$router.push('/memories');
    }
  }
}
</script>

<style scoped>

</style>