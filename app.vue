<script setup>
definePageMeta({
    pageTransition: {
        name: 'page',
        mode: 'default'
    }
})
</script>
<template>
    <div class="app-wrapper">
        <NuxtPage class="page"/>
    </div>
</template>
<style lang="scss">
.app-wrapper {
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.page {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
}

.page-enter-active,
.page-leave-active {
  transition: transform 0.2s ease, opacity 0.5s ease;
}

.page-enter-from,.page-leave-to{
  opacity: 0;
  transform: translateY(-5px);
}

</style>