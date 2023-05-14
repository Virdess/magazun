<template>
    <div class="loginform">
        <ion-item>
            <ion-input ref="input" type="email" label="Email" label-placement="floating" helper-text="Enter a valid email"
                error-text="Invalid email" @ionInput="validate" @ionBlur="markTouched"></ion-input>
        </ion-item>
        <ion-item style="margin-top:10px">
            <ion-input type="password" label="Password" label-placement="floating"
                helper-text="Enter a valid password"></ion-input>
        </ion-item>

        <ion-button fill="outline" href="folder/Главная">Войти</ion-button>
    </div>
</template>

<script setup lang="ts">
import { IonItem, IonInput, IonButton } from '@ionic/vue';
</script>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    components: { IonInput },
    methods: {
        validateEmail(email) {
            return email.match(
                /^(?=.{1,254}$)(?=.{1,64}@)[a-zA-Z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-zA-Z0-9!#$%&'*+/=?^_`{|}~-]+)*@[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?(?:\.[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?)*$/
            );
        },

        validate(ev) {
            const value = ev.target.value;

            this.$refs.input.$el.classList.remove('ion-valid');
            this.$refs.input.$el.classList.remove('ion-invalid');

            if (value === '') return;

            this.validateEmail(value)
                ? this.$refs.input.$el.classList.add('ion-valid')
                : this.$refs.input.$el.classList.add('ion-invalid');
        },

        markTouched() {
            this.$refs.input.$el.classList.add('ion-touched');
        },
    },
});
</script>

<style>
.loginform {
    width: 95%;
    text-align: center;
    margin: auto;
}
</style>