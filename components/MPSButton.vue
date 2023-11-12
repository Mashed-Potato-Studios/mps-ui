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
<!--    <slot name="leading" :disabled="props.disabled">-->
<!--      <v-icon v-if="props.isLeading && props.iconLeading"></v-icon>-->
<!--    </slot>-->
    <slot>
      <span v-if="props.text" :class="[props.truncate ? 'text-left break-all' : '']">
        {{ props.text }}
      </span>
    </slot>
  </v-btn>
</template>
