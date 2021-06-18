<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blankkkkk</ion-title>
      </ion-toolbar>
    </ion-header>
    <!-- <IonButton color="primary">Test</IonButton> -->
    <ion-tabs
      @ionTabsWillChange="beforeTabChange"
      @ionTabsDidChange="afterTabChange"
    >
      <ion-tab-bar>
        <ion-tab-button tab="schedule" href="/home">
          <ion-icon :icon="calendar"></ion-icon>
          <ion-label>Schedule</ion-label>
          <ion-badge>6</ion-badge>
        </ion-tab-button>

        <ion-tab-button tab="speakers" href="/home">
          <ion-icon :icon="personCircle"></ion-icon>
          <ion-label>Speakers</ion-label>
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
    <!-- <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blankzzzz</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <div id="container">
        <strong>Ready to create an app?</strong>
        <p>Start with Ionic <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">UI Components</a></p>
      </div>
    </ion-content> -->
  </ion-page>
</template>

<script lang="ts">
import { calendar, personCircle } from 'ionicons/icons';
import {
//   IonContent,
  IonHeader,
  IonPage,
  IonTitle,
  IonToolbar,
       IonIcon, 
  IonLabel, 
  IonTabBar, 
  IonTabButton, 
  IonTabs,
  IonBadge
//   IonButton
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Home",
  components: {
    // IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
     IonIcon, 
  IonLabel, 
  IonTabBar, 
  IonTabButton, 
  IonTabs,
  IonBadge
//   IonButton
  },
      setup() {
    const beforeTabChange = () => {
      // do something before tab change
    }
    const afterTabChange = () => {
      // do something after tab change
    }
    return {
      calendar,
      personCircle,
      beforeTabChange,
      afterTabChange
    }
  }
});
</script>

<style scoped>
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
