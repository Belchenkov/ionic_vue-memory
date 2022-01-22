<template>
  <ion-list>
    <memory-list-item
        :memory="memory"
        v-for="memory in memories"
        :key="memory.id"
    />
  </ion-list>
</template>

<script>
import { IonList } from "@ionic/vue";

import MemoryListItem from "./MemoryListItem";

export default {
  name: "MemoriesList",
  props: [
      'memories'
  ],
  components: {
    IonList,
    MemoryListItem
  },
}
</script>

<style scoped>

</style>