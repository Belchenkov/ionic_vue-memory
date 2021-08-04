<template>
  <base-layout
      page-title="Add a Memory"
      page-default-back-link="/memories"
  >
    <form class="ion-padding">
      <ion-list>
        <ion-item>
          <ion-label position="floating">Title</ion-label>
          <ion-input type="text" required clear-input />
        </ion-item>
        <ion-item>
          <ion-label position="floating">Image URL</ion-label>
          <ion-input type="url" required clear-input />
        </ion-item>
        <ion-item>
          <ion-label position="floating">Description</ion-label>
          <ion-textarea rows="5" />
        </ion-item>
        <ion-button expand="block">
          <ion-icon slot="start" :icon="save"></ion-icon>
          Save
        </ion-button>
      </ion-list>
    </form>
  </base-layout>
</template>

<script>
import {
  IonList,
  IonItem,
  IonLabel,
  IonInput,
  IonTextarea,
  IonButton,
  IonIcon
} from "@ionic/vue";
import { save } from 'ionicons/icons';

export default {
  name: "AddMemoryPage",
  components: {
    IonList,
    IonItem,
    IonLabel,
    IonInput,
    IonTextarea,
    IonButton,
    IonIcon
  },
  data() {
    return {
      save
    }
  }
}
</script>

<style scoped>

</style>