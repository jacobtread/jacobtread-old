<script setup lang="ts">

interface Properties {
    text: string,
    author: string,
}

const {text, author} = defineProps<Properties>();

</script>
<template>
    <div class="quote">
        <svg
                class="quote__mark"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                height="32px"
                width="32px"
                fill="currentColor"
        >
            <path d="M0 0h24v24H0z" fill="none"/>
            <path d="M6 17h3l2-4V7H5v6h3zm8 0h3l2-4V7h-6v6h3z"/>
        </svg>
        <p class="quote__text">{{ text }}</p>
        <span class="quote__author"
        ><span class="quote__author__dash">-</span>{{ author }}</span
        >
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.quote {
  max-width: 500px;
  display: block;
  padding: 1em;

  &__mark {
    display: block;
    margin: 0 auto;
    color: darken($text-color, 10);
  }

  &__text {
    color: $text-color;
    font-weight: 400;
    line-height: 1.5;
    text-align: center;
  }

  &__author {
    position: relative;
    display: block;
    text-align: center;
    color: darken($text-color, 5);
    margin-top: 1em;
    font-size: 0.95em;

    &__dash {
      margin-right: 1em;
    }
  }
}
</style>