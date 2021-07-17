<template>
  <ion-page>
    <ion-header>
      <ion-toolbar class="ion-text-uppercase">
          <ion-row>
            <ion-col size="2" class="ion-text-center">
               <img src="https://img.icons8.com/fluent/32/000000/noticeboard.png"/>
            </ion-col>
            <ion-col size="10" class="ion-text-start">
                <ion-text>
                      All Memories
                </ion-text>
            </ion-col>
          </ion-row>
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
    IonContent,
    IonToolbar,
    IonList,
    IonRow,
    IonCol,
    IonText,
    IonItem
} from "@ionic/vue";

export default {
  name: "MemoriesPage",
  components: {
    IonContent,
    IonText,
    IonPage,
    IonHeader,
    IonToolbar,
    IonList,
    IonRow,
    IonCol,
    IonItem
  }
}
</script>

<style scoped>
  ion-text {
    font-weight: bold;
    font-size: 1.25rem;
    font-family: 'Ultra', serif;

  }

  ion-row {
    display: flex;
    align-items: center;
  }
</style>