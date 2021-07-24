<template>
  <base-layout page-title="All Memories">
      <ion-list>
        <ion-item
            v-for="memory in memories"
            :router-link="`/memories/${memory.id}`"
            :key="memory.id"
        >
          <ion-thumbnail slot="start">
            <ion-img :src="memory.image" :alt="memory.title" />
          </ion-thumbnail>
          {{ memory.title }}
        </ion-item>
      </ion-list>
  </base-layout>
</template>

<script>
import {
    IonList,
    IonItem,
    IonImg,
    IonThumbnail
} from "@ionic/vue";

export default {
  name: "MemoriesPage",
  components: {
    IonList,
    IonItem,
    IonImg,
    IonThumbnail
  },
  data() {
    return {

    }
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