<script setup lang="ts">
/**
 * @name MPSCard
 * @description
 *
 */

export type MPSCardProps = {
  title: string;
  subtitle: string;
  loading: boolean;
  maxWidth: number;
  minWidth: number;
  maxHeight: number;
  minHeight: number;
  elevation: number;
  activeClass: boolean;
  color: string;
  isActive: boolean;

}

const props = defineProps<MPSCardProps>()
</script>
<template>
  <v-card>
    <slot name="loader"/>
    <v-card-item>
      <v-card-title>
        <span class="headline">{{ title }}</span>
      </v-card-title>
      <v-card-subtitle>{{ subtitle }}</v-card-subtitle>
    </v-card-item>
    <v-card-text>
        <slot></slot>
      </v-card-text>
  </v-card>
</template>
