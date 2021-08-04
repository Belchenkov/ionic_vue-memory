<template>
  <base-layout page-title="All Memories">
    <template v-slot:add-btn>
      <ion-button
          router-link="/memories/add"
          shape="round"
          color="dark"
      >
        <ion-icon slot="icon-only" :icon="add"></ion-icon>
      </ion-button>
    </template>
    <memories-list :memories="memories" />
  </base-layout>
</template>

<script>
import MemoriesList from "../compoents/memories/MemoriesList";
import {
  IonButton,
  IonIcon
} from "@ionic/vue";
import { add } from 'ionicons/icons';

export default {
  name: "MemoriesPage",
  components: {
    MemoriesList,
    IonButton,
    IonIcon,
  },
  data() {
    return {
      add
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