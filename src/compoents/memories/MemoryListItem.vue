<template>
  <ion-item
      :router-link="`/memories/${memory.id}`"
      :key="memory.id"
  >
    <ion-thumbnail slot="start">
      <ion-img :src="memory.image" :alt="memory.title" />
    </ion-thumbnail>
    {{ memory.title }}
  </ion-item></template>

<script>
import { IonImg, IonItem, IonThumbnail } from "@ionic/vue";

export default {
  name: "MemoryListItem",
  props: ['memory'],
  components: {
    IonItem,
    IonImg,
    IonThumbnail
  },
}
</script>

<style scoped>

</style>