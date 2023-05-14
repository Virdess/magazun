<template>
    <ion-page>
        <ion-item>
            <ion-grid>
                <ion-row>
                    <ion-col>
                        <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/thumbnail.svg"/>
                    </ion-col>
                    <ion-col>
                        <ion-row>
                            <h1>Название товара</h1>
                        </ion-row>
                    </ion-col>
                </ion-row>
                <ion-row>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint pariatur libero dolore illo recusandae
                        quisquam voluptatibus delectus eos quae. Qui facere a repudiandae aliquam laborum?</p>
                </ion-row>
            </ion-grid>
        </ion-item>
    </ion-page>
</template>

<script setup lang="ts">
import { IonContent, IonCol, IonGrid, IonInput, IonRow, IonHeader, IonTitle, IonAccordion, IonAccordionGroup, IonItem, IonPage } from '@ionic/vue';
import ProductThumb from '../../Components/ProductThumb.vue'

</script>   