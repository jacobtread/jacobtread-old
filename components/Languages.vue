<script setup lang="ts">
import TypeScriptIcon from "@/assets/icons/langs/typescript.svg?component";
import JavascriptIcon from "@/assets/icons/langs/js.svg?component";
import KotlinIcon from "@/assets/icons/langs/kotlin.svg?component";
import JavaIcon from "@/assets/icons/langs/java.svg?component";
import GoIcon from "@/assets/icons/langs/go.svg?component";
import RustIcon from "@/assets/icons/langs/rust.svg?component";
import PythonIcon from "@/assets/icons/langs/python.svg?component";
import HTMLIcon from "@/assets/icons/langs/html.svg?component";
import CSSIcon from "@/assets/icons/langs/css.svg?component";
import SASSIcon from "@/assets/icons/langs/sass.svg?component";

// name, link, icon
type Language = [string, string, any];

console.log(import('@/assets/icons/langs/sass.svg?component'))

const contents: Language[] = [
    ['Kotlin', 'https://kotlinlang.org', KotlinIcon],
    ['Java', 'https://www.java.com/', JavaIcon],
    ['Typescript', 'https://www.typescriptlang.org/', TypeScriptIcon],
    ['Javascript', 'https://www.javascript.com/', JavascriptIcon],
    ['Go', 'https://golang.org/', GoIcon],
    ['Rust', 'https://www.rust-lang.org/', RustIcon],
    ['Python', 'https://www.python.org/', PythonIcon],
    ['HTML', 'https://en.wikipedia.org/wiki/HTML/', HTMLIcon],
    ['CSS', 'https://en.wikipedia.org/wiki/CSS/', CSSIcon],
    ['SASS', 'https://sass-lang.com/', SASSIcon],
];
</script>
<template>
    <div class="block">
        <h1 class="block__title">Languages </h1>
        <p class="block__text">
            Here's a list of languages that I can write / use comfortably
        </p>
        <div class="languages">
            <a v-for="item in contents" :href="item[1]" class="language" :title="item[0]">
                <component :is="item[2]" class="language__icon"/>
                <span class="language__name">{{item[0]}}</span>
            </a>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.languages {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  justify-content: center;
  justify-items: center;
  gap: 1rem;
  margin-top: 1rem;
}

.language {
  align-items: center;
  display: flex;
  flex-flow: column;
  text-align: center;
  text-decoration: none;

  &__icon {
    width: 42px;
    height: 42px;
    color: #f58f1e;
  }

  &__name {
    margin-top: 1rem;
    color: $text-color;
    font-weight: bold;
    font-size: 0.6rem;
  }
}
</style>