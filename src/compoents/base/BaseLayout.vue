<template>
  <ion-page>
    <ion-header>
      <ion-toolbar class="ion-text-uppercase">
        <ion-row>
          <ion-col size="2" class="ion-text-center">
            <img src="https://img.icons8.com/fluent/32/000000/noticeboard.png"/>
          </ion-col>
          <ion-col size="8" class="ion-text-start">
            <ion-text>{{ pageTitle }}</ion-text>
          </ion-col>
          <ion-col size="2">
            <ion-back-button :default-href="pageDefaultBackLink"></ion-back-button>
          </ion-col>
        </ion-row>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <slot />
    </ion-content>
  </ion-page>
</template>

<script>
import {
  IonPage,
  IonHeader,
  IonContent,
  IonToolbar,
  IonRow,
  IonCol,
  IonText,
  IonBackButton,
} from "@ionic/vue";

export default {
  props: {
    pageTitle: {
      type: String,
      required: true,
    },
    pageDefaultBackLink: {
      type: String
    }
  },
  name: "BaseLayout",
  components: {
    IonContent,
    IonText,
    IonPage,
    IonHeader,
    IonToolbar,
    IonRow,
    IonCol,
    IonBackButton
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