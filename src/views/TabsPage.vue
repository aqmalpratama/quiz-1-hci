<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="home" href="/home">
          <ion-icon :icon="home" />
        </ion-tab-button>

        <ion-tab-button tab="kolam" href="/pond">
          <ion-icon :icon="water" />
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import {
  IonTabBar,
  IonTabButton,
  IonTabs,
  IonIcon,
  IonPage,
  IonRouterOutlet,
} from "@ionic/vue";
import { home, water } from "ionicons/icons";

export default defineComponent({
  name: "TabsPage",
  components: {
    IonTabs,
    IonTabBar,
    IonTabButton,
    IonIcon,
    IonPage,
    IonRouterOutlet,
  },
  setup() {
    return {
      home,
      water,
    };
  },
});
</script>

<style scoped>
ion-page {
  --background: #252836;
}
ion-tab-bar {
  --background: #252836;
  height: 64px;
  border-radius: 16px 16px 0px 0px;
}
</style>
