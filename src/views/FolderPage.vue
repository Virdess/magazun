<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button color="primary"></ion-menu-button>
        </ion-buttons>
        <ion-title>{{ $route.params.id }}</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">{{ $route.params.id }}</ion-title>
        </ion-toolbar>
      </ion-header>

      
      <div id="container" v-if="$route.params.id == 'Главная'">
        <main-pgae/>
      </div>
      <div id="container" v-else-if="$route.params.id == 'Каталог'">
        <catalog-page/>
      </div>
      <div id="container" v-else-if="$route.params.id == 'Любимое'">
        <favorite-page/>
      </div>
      <div id="container" v-else>
        <basket-page/>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonButtons, IonContent, IonHeader, IonMenuButton, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import MainPgae from './Main/MainPgae.vue';
import CatalogPage from './Catalog/CatalogPage.vue';
import FavoritePage from './Favorite/FavoritePage.vue';
import BasketPage from './Basket/BasketPage.vue'
</script>

<style scoped>

</style>
