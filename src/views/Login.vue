<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
            <ion-title> LOGIN</ion-title>
            <ion-buttons slot="end">
                <ion-button fill="solid" @click="router.push({ name: 'Registro' })"> Registrarse </ion-button>
                </ion-buttons>
            </ion-toolbar>
        </ion-header>
        <ion-content class="ion-padding">
            <ion-item class="ion-margin-bottom" lines="none">
                <ion-input 
                    label="Usuario" 
                    label-placement="floating" 
                    class="ion-margin-top"
                    fill="outline" 
                    v-model="userStore.login.username"
                    placeholder="Enter text">
                </ion-input>
            </ion-item>
            <ion-item class="ion-margin-bottom" lines="none">
                <ion-input 
                    label="Contraseña" 
                    label-placement="floating" 
                    class="ion-margin-top"
                    fill="outline"           
                    v-model="userStore.login.password"  
                    @keyup.enter="handleLogin"
                    type="password"        
                    placeholder="Enter text">
                    
                </ion-input>
            </ion-item>
            <ion-item class="ion-margin-bottom" lines="none">
                <ion-button slot="end" size="default" @click="handleLogin"> Ingresar</ion-button>
            </ion-item>
        </ion-content>
    </ion-page>
    
</template>
<script lang="ts" setup>
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent,
     IonItem, IonInput, IonButton, IonLabel,
     IonButtons, alertController } from '@ionic/vue';
import { useUserStore } from '@/stores/user';
import { useRouter } from 'vue-router';

const userStore = useUserStore();
const router = useRouter();

function handleLogin() {
    userStore.$login().then( res => {
        router.push({ name: 'Seccion' });
        }) .catch( error => {
           alertController.create({
            header: 'Error de inicio de sesión',
            message: error.response.data.message,
            buttons: ['Continuar'],
            }).then(alert => alert.present());
        });
}
</script>