<script setup lang="ts">

import VueJSIcon from "@/assets/icons/tech/vuejs.svg?component";
import IntellijIcon from "@/assets/icons/tech/idea.svg?component";
import PhpStormIcon from "@/assets/icons/tech/phpstorm.svg?component";
import WebStormIcon from "@/assets/icons/tech/webstorm.svg?component";
import PyCharmIcon from "@/assets/icons/tech/pycharm.svg?component";
import GoLandIcon from "@/assets/icons/tech/goland.svg?component";
import LaravelIcon from "@/assets/icons/tech/laravel.svg?component";
import MySQLIcon from "@/assets/icons/tech/mysql.svg?component";
import MongoDBIcon from "@/assets/icons/tech/mongodb.svg?component";
import GitHubIcon from "@/assets/icons/tech/github.svg?component";
import GitKrakenIcon from "@/assets/icons/tech/gitkraken.svg?component";
import NestJSIcon from "@/assets/icons/tech/nestjs.svg?component";
import NuxtJSIcon from "@/assets/icons/tech/nuxtjs.svg?component";
import DockerIcon from "@/assets/icons/tech/docker.svg?component";

// name, link, icon
type Language = [string, string, any];

const contents: Language[] = [
    ['VueJS', 'https://vuejs.org/', VueJSIcon],
    ['NuxtJS', 'https://nuxtjs.org/', NuxtJSIcon],
    ['NestJS', 'https://nestjs.com/', NestJSIcon],
    ['Laravel', 'https://laravel.com/', LaravelIcon],
    ['MySQL', 'https://www.mysql.com/', MySQLIcon],
    ['MongoDB', 'https://www.mongodb.com/', MongoDBIcon],
    ['GitHub', 'https://github.com/jacobtread', GitHubIcon],
    ['GitKraken', 'https://www.gitkraken.com/', GitKrakenIcon],
    ['Docker', 'https://www.docker.com/', DockerIcon],
    ['Intellij IDEA', 'https://www.jetbrains.com/idea/', IntellijIcon],
    ['PhpStorm', 'https://www.jetbrains.com/phpstorm/', PhpStormIcon],
    ['WebStorm', 'https://www.jetbrains.com/webstorm/', WebStormIcon],
    ['PyCharm', 'https://www.jetbrains.com/pycharm/', PyCharmIcon],
    ['GoLand', 'https://www.jetbrains.com/go/', GoLandIcon],
];
</script>
<template>
    <div class="block">
        <h1 class="block__title">Technologies</h1>
        <p class="block__text">
            Here's a list of technologies that I can use comfortably
        </p>
        <div class="techs">
            <a v-for="item in contents" :href="item[1]" class="tech" :title="item[0]" target="_blank" rel="noopener">
                <component :is="item[2]" class="tech__icon"/>
                <span class="tech__name">{{ item[0] }}</span>
            </a>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.techs {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  justify-content: space-evenly;
  justify-items: center;
  gap: 1rem;
  margin-top: 1rem;
}

.tech {
  align-items: center;
  display: flex;
  flex-flow: column;
  text-align: center;
  text-decoration: none;
  transition: transform 0.2s ease;

  &:hover {
    transform: scale(1.35);
  }

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