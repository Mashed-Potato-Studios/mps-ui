<template>
  <NuxtLayout>
    <v-app>
      <MPSAside
        title="Sandra Adams"
        subtitle="sandra_a88@gmailcom"
        width="300"
        expand
        rail
        permanent
        avatar="https://randomuser.me/api/portraits/men/85.jpg"
      >
        <template #list-item>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Sandra Adams"
            subtitle="sandra_a88@gmailcom"
          />
        </template>
      </MPSAside>
      <MPSAside
        location="right"
        permanent
      >
        <template #list-item>
          <v-list>
            <v-list-item
              title="Usage"
              value="usage"
            />

            <v-list-item
              title="Slots"
              value="slots"
            />

            <v-list-item
              title="Props"
              value="props"
            />
          </v-list>
        </template>
      </MPSAside>
      <NuxtPage />
    </v-app>
  </NuxtLayout>
</template>
<script setup lang="ts">
</script>
