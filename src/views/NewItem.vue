<template>
  <ion-page>

    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-back-button default-href="/home"></ion-back-button>
        </ion-buttons>
        <ion-title>New Item</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <form action="" class="padding">
        <ion-list>
          <ion-item>
            <ion-label position="floating">Title</ion-label>
          <ion-input placeholder="placeholder"></ion-input>
        </ion-item>
          <ion-item>
            <ion-label position="floating">Description</ion-label>
          <ion-textarea rows="5" placeholder="placeholder"></ion-textarea>
        </ion-item>
        </ion-list>

        <ion-button type="submit" expand="block">Save</ion-button>
      </form>
    </ion-content>

  </ion-page>
</template>

<script>
import {
  IonBackButton,
  IonButtons,
  IonContent,
  IonHeader,
  IonPage,
  IonTitle,
  IonToolbar,
  IonInput,
  IonLabel,
  // IonCard
} from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'NewItem',
  components: {
    IonBackButton,
    IonButtons,
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonInput,
    IonLabel,
    // IonCard
  }
});
</script>