<template>
  <form class="ion-padding" @submit.prevent="submitForm">
    <ion-list>
      <ion-item>
        <ion-label position="floating">Title</ion-label>
        <ion-input v-model="memory.title" type="text" required clear-input />
      </ion-item>
      <ion-item>
        <ion-label position="floating">Image URL</ion-label>
        <ion-input v-model="memory.image" type="url" required clear-input />
      </ion-item>
      <ion-item>
        <ion-label position="floating">Description</ion-label>
        <ion-textarea v-model="memory.description" rows="5" />
      </ion-item>
      <ion-button expand="block" type="submit" class="ion-margin-top">
        <ion-icon slot="start" :icon="saveIcon"></ion-icon>
        Save
      </ion-button>
    </ion-list>
  </form>
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
import { save } from "ionicons/icons";

export default {
  name: "CreateMemoryForm",
  emits: [
      'save-memory'
  ],
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
      saveIcon: save,
      memory: {
        title: '',
        image: '',
        description: '',
      }
    }
  },
  methods: {
    submitForm() {
      this.$emit('save-memory', this.memory);
    }
  }
}
</script>

<style scoped>

</style>