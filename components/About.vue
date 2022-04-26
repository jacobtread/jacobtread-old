<script setup lang="ts">
import TypeScriptIcon from "@/assets/icons/langs/typescript.svg?component";
import VueJSIcon from "@/assets/icons/tech/vuejs.svg?component";
import KotlinIcon from "@/assets/icons/langs/kotlin.svg?component";
import JavaIcon from "@/assets/icons/langs/java.svg?component";
import GoIcon from "@/assets/icons/langs/go.svg?component";
import RustIcon from "@/assets/icons/langs/rust.svg?component";

</script>
<template>
    <div class="block">
        <h1 class="block__title">About Me</h1>
        <p class="block__text">
            I am a small time developer from 🥝 New Zealand with a lot of free time on
            my hands. I spent my days developing web applications mostly 🕹️ Dashboards
            and similar applications. But I do occasionally dip my feet into the world
            desktop applications with
            <KotlinIcon class="icon--inline"/> <span class="about__context">(Kotlin)</span> and <JavaIcon class="icon--inline"/> <span class="about__context">(Java)</span>. But I do prefer to
            use Web technologies such as
            <TypeScriptIcon class="icon--inline"/> <span class="about__context">(Typescript)</span> and
            <VueJSIcon class="icon--inline"/>
            <span class="about__context">(VueJS)</span>. I've also recently been using quite a bit of
            <RustIcon class="icon--inline"/> <span class="about__context">(Rust)</span>
            and
            <GoIcon class="icon--inline" style="width: 2em;"/> <span class="about__context">(Go)</span>
            and have been really enjoying using them
        </p>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.about__context {
  opacity: 0.55;
  font-size: 0.7em;
}

</style>