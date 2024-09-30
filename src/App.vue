<script setup>
  import FeaturesBase from './components/FeaturesBase.vue'
  import FooterBase from './components/FooterBase.vue'
  import GalleryBase from './components/GalleryBase.vue'
  import HeaderBase from './components/HeaderBase.vue'
  import HomeBase from './components/HomeBase.vue'
  import RealtorsBase from './components/RealtorsBase.vue'
  import SidebarBase from './components/SidebarBase.vue'
  import StoryBase from './components/StoryBase.vue'
</script>

<template>
  <div class="container">
    <SidebarBase />
    <HeaderBase />
    <RealtorsBase />
    <FeaturesBase />
    <StoryBase />
    <HomeBase />
    <GalleryBase />
    <FooterBase />
  </div>
</template>

<style lang="scss" scoped>
  .container {
    display: grid;
    grid-template-rows: 80vh min-content 40vw repeat(3, min-content);
    grid-template-columns:
      [sidebar-start] 8rem [sidebar-end full-start] minmax(6rem, 1fr) [center-start] repeat(
        8,
        [col-start] minmax(min-content, 14rem) [col-end]
      )
      [center-end] minmax(6rem, 1fr) [full-end];

    @media only screen and (max-width: $bp-largest) {
      grid-template-rows: 6rem 80vh min-content 40vw repeat(3, min-content);
      grid-template-columns:
        [full-start] minmax(6rem, 1fr) [center-start] repeat(8, [col-start] minmax(min-content, 14rem) [col-end])
        [center-end] minmax(6rem, 1fr) [full-end];
    }

    @media only screen and (max-width: $bp-medium) {
      grid-template-rows: 6rem calc(100vh - 6rem);
    }
  }
</style>
