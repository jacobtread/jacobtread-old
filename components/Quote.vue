<script setup lang="ts">

import QuoteIcon from "assets/icons/quote.svg?component"

interface Properties {
    text: string,
    author: string,
}

const {text, author} = defineProps<Properties>();

</script>
<template>
    <div class="quote">
        <QuoteIcon class="quote__mark"/>
        <p class="quote__text">{{ text }}</p>
        <span class="quote__author"
        ><span class="quote__author__dash">-</span>{{ author }}</span
        >
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.quote {
  max-width: 800px;
  display: block;

  &__mark {
    display: block;
    color: darken($text-color, 10);
    margin: 0 auto;
  }

  &__text {
    max-width: 600px;
    margin: 0 auto;
    color: $text-color;
    font-weight: 400;
    line-height: 1.5;
    font-size: 1rem;
  }

  &__author {
    position: relative;
    display: block;
    color: darken($text-color, 5);
    margin-top: 1em;
    font-size: 0.95em;

    &__dash {
      margin-right: 1em;
    }
  }
}
</style>