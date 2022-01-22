<template>
  <form class="ion-padding" @submit.prevent="submitForm">
    <ion-list>
      <ion-item>
        <ion-label position="floating">Title</ion-label>
        <ion-input v-model="memory.title" type="text" required clear-input />
      </ion-item>
      <ion-item>
        <ion-thumbnail
            v-if="memory.takenImageUrl"
            slot="start"
        >
          <img :src="memory.takenImageUrl" alt="">
        </ion-thumbnail>
        <ion-button
            type="button"
            fill="clear"
            @click="takePhoto"
        >
          <ion-icon
              slot="start"
              :icon="cameraIcon"
          />
          Take Photo
        </ion-button>
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
  IonIcon,
  IonThumbnail,
} from "@ionic/vue";
import { save, camera } from "ionicons/icons";
import { Camera, CameraResultType, CameraSource } from '@capacitor/camera';

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
    IonIcon,
    IonThumbnail,
  },
  data() {
    return {
      saveIcon: save,
      cameraIcon: camera,
      memory: {
        title: '',
        image: '',
        description: '',
        takenImageUrl: null,
      }
    }
  },
  methods: {
    async takePhoto() {
      const photo = await Camera.getPhoto({
        resultType: CameraResultType.Uri,
        source: CameraSource.Camera,
        quality: 60,
      });

      this.memory.takenImageUrl = photo.webPath;
    },
    submitForm() {
      this.$emit('save-memory', this.memory);
    }
  }
}
</script>

<style scoped>

</style>