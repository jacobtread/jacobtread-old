<script setup lang="ts">
import LinkIcon from "assets/icons/link.svg?component"
</script>
<template>
    <div class="heading-group__wrapper">
        <div class="heading-group">
            <NuxtLink class="button button--first" to="#about">
                <LinkIcon class="button__icon"/>
                <span class="button__text">About</span>
            </NuxtLink>
            <NuxtLink class="button button--second" to="#contact">
                <LinkIcon class="button__icon"/>
                <span class="button__text">Contact</span>
            </NuxtLink>
            <NuxtLink class="button button--second" to="projects">
                <LinkIcon class="button__icon"/>
                <span class="button__text">Projects</span>
            </NuxtLink>
            <NuxtLink class="button button--third" to="#tech">
                <LinkIcon class="button__icon"/>
                <span class="button__text">Tech</span>
            </NuxtLink>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";
@import "assets/scss/mixins";

.heading-group__wrapper {
  display: flex;
  flex-flow: row;
  justify-content: center;
  margin: 0 auto;

  @include max-width(714px) {
    display: block;
    width: calc(100% - 4rem);
    padding: 0 2rem;

    .heading-group {
      flex-flow: column;
      background: linear-gradient($first-block-tint-top, $first-block-tint-bottom, $second-block-tint-top, $second-block-tint-bottom, $third-block-tint-top, $third-block-tint-bottom);
      align-items: stretch;
    }
  }

  @include max-width(430px) {
    padding: 0 1rem;
    width: calc(100% - 2rem);
  }
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