<script setup lang="ts">
export type MPSBreadCrumbsProps = {
  items: string[];
  bgColor: string;
};
const route = useRoute();
const router = useRouter();

const props = defineProps<MPSBreadCrumbsProps>();

const crumbLinks = ref(null);

const breadCrumbs = computed(() => {
  // crumbLinks.value = getBreadCrumbs();
});
const getBreadCrumbs = () => {
  return route.matched.map((item) => {
    console.log(item);
    // Separate the path by the slashes
    const path = item.path.split("/");
    console.log(path);
    // Use path to show all the crumbs
    return path
  });
};

onMounted(() => {
  getBreadCrumbs()
})

</script>
<template>
  <v-breadcrumbs bg-color="green" :items="['Documentation', 'Components', 'MPSMain']"></v-breadcrumbs>
</template>
