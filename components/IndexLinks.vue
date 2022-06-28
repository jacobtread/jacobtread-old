<script setup lang="ts">
import LinkIcon from "assets/icons/link.svg?component"
</script>
<template>
    <div class="heading-group__wrapper">
        <div class="heading-group">
            <a class="button button--first" href="#about">
                <LinkIcon class="button__icon"/>
                <span class="button__text">About</span>
            </a>
            <a class="button button--second" href="#contact">
                <LinkIcon class="button__icon"/>
                <span class="button__text">Contact</span>
            </a>
            <NuxtLink class="button button--second" to="projects">
                <LinkIcon class="button__icon"/>
                <span class="button__text">Projects</span>
            </NuxtLink>
            <a class="button button--third" href="#tech">
                <LinkIcon class="button__icon"/>
                <span class="button__text">Tech</span>
            </a>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";

.heading-group__wrapper {
  display: flex;
  flex-flow: row;
  justify-content: center;
  margin: 0 auto;
}

.button {
  &--first {
    background: $first-button-background;
  }

  &--second {
    background: $second-button-background;
  }

  &--third {
    background: $third-button-background;
  }
}

.heading-group {
  display: flex;
  flex-flow: row;
  background: linear-gradient(90deg, $first-block-tint-top, $first-block-tint-bottom, $second-block-tint-top, $second-block-tint-bottom, $third-block-tint-top, $third-block-tint-bottom);
  justify-content: center;
  justify-items: center;
  align-items: center;
  padding: 1rem;
  gap: 1.25rem;
}

</style>