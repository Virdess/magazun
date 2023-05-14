<script lang="ts">
import LoginForm from '@/Components/LoginForm.vue';
export default {
    components: {
        LoginForm: LoginForm
    }
}
</script>
<template>
    <ion-app>
        <LoginForm/>
    </ion-app>
</template>
  
<script setup lang="ts">
import {
    IonApp,
    IonContent,
    IonIcon,
    IonItem,
    IonLabel,
    IonList,
    IonListHeader,
    IonMenu,
    IonMenuToggle,
    IonNote,
    IonRouterOutlet,
    IonSplitPane,
} from '@ionic/vue';
import { ref } from 'vue';
import {
    archiveOutline,
    archiveSharp,
    bookmarkOutline,
    bookmarkSharp,
    heartOutline,
    heartSharp,
    mailOutline,
    mailSharp,
    paperPlaneOutline,
    paperPlaneSharp,
    trashOutline,
    trashSharp,
    warningOutline,
    warningSharp,
    newspaper,
    apps,
    cart
} from 'ionicons/icons';
</script>

<style>

</style>