<template>
	<ion-page>
		<ion-header>
			<ion-toolbar>
				<ion-title>Tab 1</ion-title>
			</ion-toolbar>
		</ion-header>
		<ion-content :fullscreen="true">
			<ion-header collapse="condense">
				<ion-toolbar>
					<ion-title size="large">Tab 1</ion-title>
				</ion-toolbar>
			</ion-header>
			<ion-button @click="router.push('/tab1/child')">Go to child page</ion-button>
			<ExploreContainer name="Tab 1 page" />
		</ion-content>
	</ion-page>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonButton } from "@ionic/vue";
import ExploreContainer from "@/components/ExploreContainer.vue";
import { useRouter } from "vue-router";

export default defineComponent({
	name: "Tab1Page",
	components: { ExploreContainer, IonButton, IonHeader, IonToolbar, IonTitle, IonContent, IonPage },
	setup() {
		const router = useRouter();
		return { router };
	},
});
</script>
