<script setup lang="ts">
import type {MPSButtonProps} from "./MPSButton.vue";

export type MPSLandingSectionProps = {
  title: {
    type: String,
  };
  subtitle: string;
  image: string;
  icon: string;
  description: string;
  links: (MPSButtonProps & { click?: Function })[];
  align: "start" | "center" | "end";
  headline: string
  color: string;
  features: {
    title: string;
    description?: string;
    icon?: string;
  }[];
  // slots: {
  //   headline: {
  //     title: string;
  //     description: string;
  //     links: (MPSButtonProps & { click?: Function })[];
  //   };
  //   features: {
  //     title: string;
  //     description?: string;
  //     icon?: string;
  //   }[];
  // };
}

const props = defineProps<MPSLandingSectionProps>()

</script>
<template>
  <v-sheet class="d-flex align-center pb-16">
    <v-container class="text-center">
      <v-chip
        class="ma-2"
        :color="props.color"
      >
        {{ props.headline }}
      </v-chip>
      <h1 class="text-h1">{{ props.title }}</h1>
      <p class="mt-4 text-medium-emphasis">{{ props.description }}</p>
      <v-list v-if="props.features">
        <v-list-item
          v-for="(feature, i) in props.features"
          :key="i">
          <p>{{ feature.title }}</p>
            <v-icon>{{ feature.icon }}</v-icon>
          <p>{{ feature.description }}</p>
        </v-list-item>
      </v-list>
      <slot name="headline" />
      <slot name="image" />
      <slot name="title" />
      <slot name="description" />
      <slot name="links" />

    </v-container>
  </v-sheet>
</template>
