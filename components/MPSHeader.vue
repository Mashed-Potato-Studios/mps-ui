<script setup lang="ts">


interface HeaderProps {
  links: { text: string; to: string }[]
  headerTitle: string;
}

const props = defineProps<HeaderProps>()
</script>
<template>
  <v-app-bar app>
    <slot name="logo">
      <v-toolbar-title>{{ props.headerTitle }}</v-toolbar-title>
    </slot>
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn v-for="link in props.links" :key="link.text">
        <NuxtLink :to="link.to">{{ link.text }}</NuxtLink>
      </v-btn>
    </v-toolbar-items>
    <v-spacer></v-spacer>
    <slot name="actions">
      <v-btn><v-icon icon="mdi-github" size="x-large"></v-icon></v-btn>
      <v-btn><v-icon icon="mdi-magnify" size="x-large"></v-icon></v-btn>
      <v-btn><v-icon icon="mdi-motion" size="x-large"></v-icon></v-btn>
    </slot>
  </v-app-bar>
</template>
<style scoped>
a {
  color: inherit;
  text-decoration: none;
}
</style>

