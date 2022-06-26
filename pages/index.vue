<script setup lang="ts">

import HLeft from "assets/img/hleft.svg?component";
import HRight from "assets/img/hright.svg?component";
</script>
<template>
    <div>
        <Heading text="Contact" link="contact"/>
        <main class="main">
            <About/>
        </main>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";
@import "assets/scss/mixins";

.content {
  max-width: 1000px;
  margin: 1rem auto;
}

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
</style>