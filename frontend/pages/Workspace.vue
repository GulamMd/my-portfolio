<template>
  <div class="container">
    <AppBanner />
    <Topbar></Topbar>
  </div>
</template>

<script>
import Topbar from '../components/Topbar.vue';
import AppBanner from '../components/AppBanner.vue'

export default {
    name: "Workspace",
    components: { Topbar, AppBanner }
}
</script>

<style>

</style>