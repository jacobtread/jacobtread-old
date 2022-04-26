<script setup lang="ts">

import HLeft from "assets/img/hleft.svg?component";
import HRight from "assets/img/hright.svg?component";


</script>
<template>
    <HLeft class="graphic graphic--left"/>
    <HRight class="graphic graphic--right"/>
    <Heading/>
    <About/>
    <Languages/>
</template>
<style lang="scss" scoped>
@import "assets/scss/variables";
@import "assets/scss/mixins";

.graphic {
  position: absolute;
  z-index: -1;
  max-width: 100%;
  height: 100%;

  &--left {
    left: 0;
    top: 0;
  }

  &--right {
    right: 0;
    top: 100%;
  }
}

.quote {
  opacity: 0.95;
}


</style>
