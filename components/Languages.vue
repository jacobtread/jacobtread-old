<script setup lang="ts">
import TypeScriptIcon from "@/assets/icons/typescript.svg?component";
import JavascriptIcon from "@/assets/icons/js.svg?component";
import VueJSIcon from "@/assets/icons/vuejs.svg?component";
import KotlinIcon from "@/assets/icons/kotlin.svg?component";
import JavaIcon from "@/assets/icons/java.svg?component";
import GoIcon from "@/assets/icons/go.svg?component";
import RustIcon from "@/assets/icons/rust.svg?component";
import PythonIcon from "@/assets/icons/python.svg?component";
import IntellijIcon from "@/assets/icons/idea.svg?component";
import HTMLIcon from "@/assets/icons/html.svg?component";
import CSSIcon from "@/assets/icons/css.svg?component";
import SASSIcon from "@/assets/icons/sass.svg?component";
import LaravelIcon from "@/assets/icons/laravel.svg?component";
import MySQLIcon from "@/assets/icons/mysql.svg?component";
import MongoDBIcon from "@/assets/icons/mongodb.svg?component";

// name, link, icon
type Language = [string, string, any];

const contents: Language[] = [
    ['Kotlin', 'https://kotlinlang.org', KotlinIcon],
    ['Java', 'https://www.java.com/', JavaIcon],
    ['VueJS', 'https://vuejs.org/', VueJSIcon],
    ['Typescript', 'https://www.typescriptlang.org/', TypeScriptIcon],
    ['Javascript', 'https://www.javascript.com/', JavascriptIcon],
    ['Go', 'https://golang.org/', GoIcon],
    ['Rust', 'https://www.rust-lang.org/', RustIcon],
    ['Python', 'https://www.python.org/', PythonIcon],
    ['HTML', 'https://en.wikipedia.org/wiki/HTML/', HTMLIcon],
    ['CSS', 'https://en.wikipedia.org/wiki/CSS/', CSSIcon],
    ['SASS', 'https://sass-lang.com/', SASSIcon],
    ['Laravel', 'https://laravel.com/', LaravelIcon],
    ['MySQL', 'https://www.mysql.com/', MySQLIcon],
    ['MongoDB', 'https://www.mongodb.com/', MongoDBIcon],
    ['Intellij IDEA', 'https://www.jetbrains.com/', IntellijIcon],
];
</script>
<template>
    <div class="block">
        <h1 class="block__title">Languages & Technologies</h1>
        <p class="block__text">
            Here's a list of languages / technologies that I can write / use comfortably
        </p>
        <div class="languages">
            <a v-for="item in contents" :href="item[1]" class="language">
                <component :is="item[2]" class="language__icon"/>
                <span class="language__name">{{ item[0] }}</span>
            </a>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.languages {
  display: flex;
  flex-flow: row wrap;
  align-items: stretch;
  justify-content: center;
  gap: 1rem;
}

.language {
  align-items: center;
  padding: 1rem;
  display: flex;
  flex-flow: column;
  align-items: center;
  text-align: center;
  background: $background-light;

  max-width: 100px;
  max-height: 200px;
  width: 100%;

  flex: auto;


  &__icon {
    height: 52px;
    width: 100%;
    max-width: 52px;
    color: #f58f1e;
  }

  &__name {
    margin-top: 1rem;
    color: $text-color;
    font-weight: bold;
  }

}
</style>