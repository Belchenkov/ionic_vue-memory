<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>
          <img src="https://img.icons8.com/cute-clipart/34/000000/copybook.png" />
          All Memories
        </ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <ion-list>
        <ion-item>1</ion-item>
        <ion-item>2</ion-item>
        <ion-item>3</ion-item>
      </ion-list>
    </ion-content>
  </ion-page>
</template>

<script>
import {
    IonPage,
    IonHeader,
    IonTitle,
    IonContent,
    IonToolbar,
    IonList,
    IonItem
} from "@ionic/vue";

export default {
  name: "MemoriesPage",
  components: {
    IonContent,
    IonTitle,
    IonPage,
    IonHeader,
    IonToolbar,
    IonList,
    IonItem
  }
}
</script>

<style scoped>
  ion-title {
    font-weight: bold;
    font-family: 'Ultra', serif;
  }
</style>