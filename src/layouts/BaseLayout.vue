<template>
    <ion-page>
        <ion-menu content-id="main-content">
            <ion-header>
            <ion-toolbar>
                <ion-title>Menu Content</ion-title>
            </ion-toolbar>
    </ion-header>
    <ion-content>
                    <ion-accordion-group>
                <ion-accordion value="first">
                <ion-item slot="header" color="light">
                    <ion-label>First Accordion</ion-label>
                </ion-item>
                <div slot="content"><ion-list>
                        <ion-item>
                        <ion-label>Pokémon Yellow</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>Mega Man X</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>The Legend of Zelda</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>Pac-Man</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>Super Mario World</ion-label>
                        </ion-item>
                    </ion-list></div>
                </ion-accordion>
                <ion-accordion value="second">
                <ion-item slot="header" color="light">
                    <ion-label>Second Accordion</ion-label>
                </ion-item>
                <div slot="content"><ion-list>
                        <ion-item>
                        <ion-label>Pokémon Yellow</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>Mega Man X</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>The Legend of Zelda</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>Pac-Man</ion-label>
                        </ion-item>
                        <ion-item>
                        <ion-label>Super Mario World</ion-label>
                        </ion-item>
                    </ion-list></div>
                </ion-accordion>
                <ion-accordion value="third">
                <ion-item slot="header" color="light">
                    <ion-label>Third Accordion</ion-label>
                </ion-item>
                <div slot="content"><ion-list>
                            <ion-item>
                            <ion-label>Pokémon Yellow</ion-label>
                            </ion-item>
                            <ion-item>
                            <ion-label>Mega Man X</ion-label>
                            </ion-item>
                            <ion-item>
                            <ion-label>The Legend of Zelda</ion-label>
                            </ion-item>
                            <ion-item>
                            <ion-label>Pac-Man</ion-label>
                            </ion-item>
                            <ion-item>
                            <ion-label>Super Mario World</ion-label>
                            </ion-item>
                        </ion-list></div>
    </ion-accordion>
  </ion-accordion-group>
        .</ion-content>
  </ion-menu>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button></ion-menu-button>
        </ion-buttons>
        <ion-title>Menu</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content id="main-content" class="ion-padding"> Tap the button in the toolbar to open the menu. </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
  import { IonButtons, IonContent, IonHeader, IonMenu, IonMenuButton, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
  import { IonAccordion, IonAccordionGroup, IonItem, IonLabel, IonList } from '@ionic/vue';

</script>   