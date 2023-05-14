<template>
    <img src="/photo_5402482741817231396_y.jpg" style="margin: 0 auto; display: block;" />
    <ion-title style="margin-top: 15px;">
        Топ:
    </ion-title>

    <ion-accordion-group>
        <ion-accordion value="first">
            <ion-item slot="header" color="light">
                <ion-label>Новинки</ion-label>
            </ion-item>
            <ProductThumb slot="content" v-for="prod in topProds" :title="prod.title" :desc="prod.desc" :price="prod.price" />
        </ion-accordion>
        <ion-accordion value="second">
            <ion-item slot="header" color="light">
                <ion-label>Одежда</ion-label>
            </ion-item>
            <ProductThumb slot="content" v-for="prod in topProds" :title="prod.title" :desc="prod.desc" :price="prod.price" />
        </ion-accordion>
        <ion-accordion value="third">
            <ion-item slot="header" color="light">
                <ion-label>Обувь</ion-label>
            </ion-item>
            <ProductThumb slot="content" v-for="prod in topProds" :title="prod.title" :desc="prod.desc" :price="prod.price" />
        </ion-accordion>
    </ion-accordion-group>
</template>

<script setup lang="ts">
import { IonContent, IonCol, IonGrid, IonInput, IonRow, IonHeader, IonTitle, IonAccordion, IonAccordionGroup, IonItem } from '@ionic/vue';
import ProductThumb from '../../Components/ProductThumb.vue'

let topProds = {
    prod1: {
        title: 'Товар 1',
        desc: 'Краткое описание товавра 1 Краткое описание товавра 1 Краткое описание товавра 1 Краткое описание товавра 1',
        price: 121
    },
    prod2: {
        title: 'Товар 2',
        desc: 'Краткое описание товавра 2 Краткое описание товавра 2 Краткое описание товавра 2 ',
        price: 51351
    },
    prod3: {
        title: 'Товар 3',
        desc: 'Краткое описание товавра 3 Краткое описание товавра 3 Краткое описание товавра 3 Краткое описание товавра 3 ',
        price: 987
    },
    prod4: {
        title: 'Товар 4',
        desc: 'Краткое описание товавра 4 Краткое описание товавра 4 Краткое описание товавра 4 Краткое описание товавра 4 ',
        price: 624
    },
    prod5: {
        title: 'Товар 5',
        desc: 'Краткое описание товавра 5 Краткое описание товавра 5 Краткое описание товавра 5 Краткое описание товавра 5 ',
        price: 236236
    },
}
</script>   