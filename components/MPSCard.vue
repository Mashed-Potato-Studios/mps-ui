<script setup lang="ts">
/**
 * @name MPSCard
 * @description
 *
 */



</script>
<template>
  <v-card>
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
