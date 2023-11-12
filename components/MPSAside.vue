<script setup lang="ts">
/**
 * @description MPSAside is use to create a aside menu. It takes a slot of "list-item"
 */

/**
 *
 */
export type IAsideProps = {
  title: string;
  subtitle: string;
  icon: string;
  avatar?: string;
  width: number;
  rail?: boolean
  permanent?: boolean
  expand?: boolean;
  location?: "end" | "start" | "left" | "top" | "bottom" | "right" |undefined;
}

const props = defineProps<IAsideProps>()
</script>
<template>
  <v-navigation-drawer
    :width="props.width"
    :expand-on-hover="props.expand"
    :rail="props.rail"
    :permanent="props.permanent"
    :location="props.location"
  >
    <v-list>
      <v-list>
        <!--            <v-list-item-->
        <!--              prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"-->
        <!--              title="Sandra Adams"-->
        <!--              subtitle="sandra_a88@gmailcom"-->
        <!--            ></v-list-item>-->
        <slot name="list-item" />
      </v-list>
    </v-list>
  </v-navigation-drawer>
</template>
