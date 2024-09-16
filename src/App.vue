<template>
  <div id="app" class="p-6">
    <div class="container mx-auto">
      <ProjectInfoComponent />
      <PropertySelectionComponent />
      <RecordsTableComponent />
      <MobileWorkComponent />
    </div>
  </div>
</template>

<script>
import ProjectInfoComponent from "./components/ProjectInfoComponent.vue";
import PropertySelectionComponent from "./components/PropertySelectionComponent.vue";
import RecordsTableComponent from "./components/RecordsTableComponent.vue";
import MobileWorkComponent from "./components/MobileWorkComponent.vue";

export default {
  name: "App",
  components: {
    ProjectInfoComponent,
    PropertySelectionComponent,
    RecordsTableComponent,
    MobileWorkComponent,
  },
};
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css";
</style>
