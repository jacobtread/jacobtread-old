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
        <h1 class="heading__corner">JR <span class="heading__corner__sub">My Projects</span></h1>

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
    width: 100%; // Heading must span the entire available width


    /* Background image of code with linear-gradient in-front of it*/
    background: linear-gradient($heading-gradient-start, $heading-gradient-end) no-repeat center,
    url("assets/img/background.png") no-repeat center;
    background-size: cover;

    &__corner {
        padding: 1rem;
        display: flex;
        flex-flow: row;
        gap: 1rem;
        align-items: center;


        font-size: 3rem;
        color: white;
        font-weight: bold;

        &__sub {
            font-size: 1.5rem;
            font-weight: 400;
        }
    }
}

</style>