<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>List A</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true" color="success">
      <ion-card>
        <ion-card-content color="success">
      <ion-list class="padding">
        <ion-item v-for="(item, i) in lists" :key="i">
          <ion-card>
            <ion-card-header>
              <ion-card-title>{{ item.Title }}</ion-card-title>
              <ion-card-subtitle>{{ item.Description }}</ion-card-subtitle>
            </ion-card-header>

            <ion-card-content>
              Keep close to Nature's heart... and break clear away, once in awhile,
              and climb a mountain or spend a week in the woods. Wash your spirit clean.
            </ion-card-content>
          </ion-card>
        </ion-item>
      </ion-list>
        </ion-card-content>
      </ion-card>
     
      <ion-fab vertical="bottom" horizontal="end" slot="fixed">
        <ion-fab-button @click="() => router.push('/new')">
          <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
      </ion-fab>
     
    </ion-content>
  </ion-page>
</template>

<script>
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonFab, IonCard, IonCardSubtitle, IonCardTitle, IonList, IonItem } from '@ionic/vue';
import { defineComponent } from 'vue';
import { add } from 'ionicons/icons';
import { useRouter } from 'vue-router';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonFab, IonCard, IonCardSubtitle, IonCardTitle,
    IonList,
    IonItem
  },
  setup() {
    return {
      router: useRouter(),
      add
    }
  },
  data: () => {
    return {
     lists: [
       { Id: 1, Title: 'ToDo', Description: 'To Do List'},
       { Id: 2, Title: 'Music', Description: 'Music List'},
       { Id: 3, Title: 'Movies', Description: 'Movie List'},
       { Id: 4, Title: 'Other Stuff', Description: 'Other stuff'},
     ]
    }
  }
});
</script>

<style scoped>
.ion-background-color {
  --ion-background-color: red;
}
.item-background-color{
    --ion-item-background:white;
}
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>