<script setup lang="ts">
import TypeScriptIcon from "@/assets/icons/typescript.svg?component";
import VueJSIcon from "@/assets/icons/vuejs.svg?component";
import KotlinIcon from "@/assets/icons/kotlin.svg?component";
import JavaIcon from "@/assets/icons/java.svg?component";
import GoIcon from "@/assets/icons/go.svg?component";
import RustIcon from "@/assets/icons/rust.svg?component";

</script>
<template>
    <div class="block">
        <h1 class="block__title">About Me</h1>
        <p class="block__text">
            I am a small time developer from 🥝 New Zealand with a lot of free time on
            my hands. I spent my days developing web applications mostly 🕹️ Dashboards
            and similar applications. But I do occasionally dip my feet into the world
            desktop applications with
            Kotlin <KotlinIcon class="icon--inline"/> and Java <JavaIcon class="icon--inline"/>. But I do prefer to
            use Web technologies such as
            <TypeScriptIcon class="icon--inline"/>
            Typescript and
            <VueJSIcon class="icon--inline"/>
            VueJS. I've also recently been using Rust
            <RustIcon class="icon--inline"/>
            and
            Go <GoIcon class="icon--inline" style="width: 2em;"/>
            and have been really enjoying using them
        </p>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

</style>