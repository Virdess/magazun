<template>
    <ion-grid>
        <router-link :to="{name:'ProductPage', params:{id:title}}" style="text-decoration: none; color: #000;">
            <ion-row>
                <ion-thumbnail>
                    <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/thumbnail.svg" />
                </ion-thumbnail>
                <ion-col>{{ title }}</ion-col>
                <ion-col size="auto">
                    <div style="width: 80px; text-align: end;">${{ price }}</div>
                </ion-col>
            </ion-row>
            <ion-row>
                <ion-card-subtitle>{{ desc }}</ion-card-subtitle>
            </ion-row>
        </router-link>

    </ion-grid>
</template>
<script setup lang="ts">
import { IonContent, IonCol, IonGrid, IonInput, IonRow, IonThumbnail } from '@ionic/vue';
import { RouterLink } from 'vue-router';

defineProps({
    title: String,
    desc: String,
    price: Number
});
</script>