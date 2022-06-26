<script setup lang="ts">

interface Properties {
    link: string,
    text: string,
}

const { link, text } = defineProps<Properties>()

const TYPER_VALUES: string[] = [
    'Full-Stack', 'Web', 'Kotlin', 'Front-end',
    'Back-end', 'Stonks™', 'JS', 'PHP', 'Go', 'Rust',
    'Cool', 'Bad', 'Cheat', 'HTML', 'CSS', '!Good',
]
</script>
<template>
    <div class="heading">
        <h1 class="heading__corner">JR</h1>
        <div class="heading__content">
            <img class="heading__content__img" src="assets/img/banner.png" alt="Banner Image"/>
            <h1 class="heading__content__title">Jacob Read</h1>
            <p class="heading__content__text">
                I am a
                <Typer class="heading__content__text__role" :values="TYPER_VALUES" :duration="1000"/>
                Developer
            </p>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";
@import "assets/scss/mixins";
@import "assets/scss/colors";

/* Heading element */
.heading {
    margin: 0;
    padding: 0;
    display: flex;
    width: 100%; // Heading must span the entire available width
    height: 100vh; // Heading must take up the entire viewport

    flex-flow: column;
    justify-content: center;
    align-items: center;

    /* Background image of code with linear-gradient in-front of it*/
    background: linear-gradient($heading-gradient-start, $heading-gradient-end) no-repeat center,
    url("assets/img/background.png") no-repeat center;
    background-size: cover;

    &__corner {
        position: fixed;
        left: 1rem;
        top: 1rem;
        font-size: 3rem;
        color: white;
        font-weight: bold;
    }


    &__content {
        text-align: center;

        &__img {
            opacity: 0.7;
            margin-bottom: 1rem;
        }

        &__title {
            color: $heading-title;
            margin-bottom: 1rem;
            font-weight: 400;
            font-size: 4rem;
        }

        &__text {
            color: $heading-text;
            font-size: 1.5rem;

            &__role {
                color: $heading-role;
                font-weight: bold;
            }
        }
    }
}

</style>