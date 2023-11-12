<script setup lang="ts">/**
 * @description The MPSLandingHero component will wrap your content in a Container component and apply a full width to the main element.
 */
import type { MPSButtonProps } from "./MPSButton.vue";

interface IMPSLandingHero {
  headline?: {
    // badge?: MPSBadge,
    button?: MPSButtonProps,
    title: string,
  }
  title: string;
  description: string;
  links?: { text: string; to: string }[];
  orientation?: "left" | "right";
}

const props = defineProps<IMPSLandingHero>();
</script>
<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="6">
        <h1>{{ props.title }}</h1>
        <p>{{ props.description }}</p>
        <slot />
      </v-col>
      <slot :name="props.links" />
    </v-row>
  </v-container>
</template>
