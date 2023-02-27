<template>
  <div class="flex h-screen">
    <div v-if="!showSidebar" class="w-200 bg-gray-100">
      <MenuIcon class="h-12 w-12 text-gray-500" @click="toggleSidebar" />
    </div>
    <div v-else class="w-600 bg-gray-100">
      <MenuIcon class="h-12 w-12 text-gray-500" @click="toggleSidebar" />
    </div>
  </div>
</template>

<script>
import { MenuIcon } from "vue-feather-icons";
export default {
  name: "Sidebar",
  components: { MenuIcon },
  data() {
    return {
      showSidebar: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.showSidebar = !this.showSidebar;
    },
  },
};
</script>

<style>
.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(-100%);
}
</style>