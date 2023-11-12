<script setup lang="ts">
const feature = [{ title: 'Fully customizable', description: 'Like Nuxt UI, change the style of any component from your App Config or customize them specifically through the ui prop.', icon: 'mdi-checkbox-marked-circle' }, { title: 'Slots for everything', description: 'Each component leverages the power of Vue slots to give you the flexibility to build anything.', icon: 'mdi-minus-circle' }]
</script>
<template>
  <MPSMain>
    <MPSHeader header-title="MPS"/>
    <MPSLandingHero title="MPS UI" description="MPS UI is Nuxt Layer built with Vuetify Components" />
    <MPSLandingSection title="MPS UI" description="MPS UI is Nuxt Layer built with Vuetify Components. The layer ships with an extensive amount of components." headline="MPS" align="center" color="red" :features="feature">
      <template #image>
        <v-responsive>
          <v-img src="https://images.unsplash.com/photo-1699541948287-9c8ce85624ce?q=80&w=1287&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" height="500"
              />
        </v-responsive>
      </template>
    </MPSLandingSection>
  </MPSMain>
</template>
<script setup lang="ts">
</script>
