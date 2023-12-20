<script setup lang="ts">
export type MPSButtonProps = {
  text: string;
  iconLeading: string;
  disabled: boolean;
  truncate: boolean;
  isLeading: boolean;
}

const props = defineProps<MPSButtonProps>()
</script>
<template>
  <v-btn>
    <slot>
      <span v-if="props.text" :class="[props.truncate ? 'text-left break-all' : '']">
        {{ props.text }}
      </span>
    </slot>
    <slot name="icon">
      <v-icon v-if="props.iconLeading" :left="props.isLeading">{{ props.iconLeading }}</v-icon>
    </slot>
  </v-btn>
</template>
