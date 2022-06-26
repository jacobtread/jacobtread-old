<script setup lang="ts">

    import LinkIcon from "assets/icons/link.svg?component"
    import GithubIcon from "assets/icons/tech/github.svg?component"

</script>
<template>
    <div class="content--background">
        <div class="content" id="about">
            <a class="content__title" href="#about">Getting to know me</a>
            <div class="content__body">
                <div class="content__body__item">
                    <h2 class="content__body__item__title">
                        <span class="content__body__item__title__prefix">#</span>
                        My History
                    </h2>
                    <p class="content__body__item__text">
                        I’ve grown up in and spent my entire life in New Zealand. From the ripe young age of 11
                        I’ve always had a great interest in programming and have spent a majority of my time learning
                        and building up my skills with different programming languages, frameworks, and toolsets.
                        My earliest programming adventures came about from the early days of Minecraft modding.
                    </p>
                </div>
                <div class="content__body__item">
                    <h2 class="content__body__item__title">
                        <span class="content__body__item__title__prefix">#</span>
                        My Interests
                    </h2>
                    <p class="content__body__item__text">
                        I am very interested in learning programming related subjects as I have spent almost of all my education career
                        following the programming pathways. I quite enjoy working with other peoples code through reverse engineering and
                        other collaboration. Outside of programming I am also interested in body building and I like to keep a strict routine
                        with my exercise.
                    </p>
                </div>
                <div class="content__body__item">
                    <h2 class="content__body__item__title">
                        <span class="content__body__item__title__prefix">#</span>
                        Projects
                    </h2>
                    <p class="content__body__item__text">
                        I’ve worked on many projects throughout the years many of which are readily available on my Github the projects listed on
                        my github are majority under the MIT license. My projects come in all kinds of varieties in all different kinds of langauges
                        and frameworks. Feel free to take a look around and see if any of them spark your interests
                    </p>
                </div>
            </div>
            <div class="button-group">
                <NuxtLink class="button" to="projects">
                    <LinkIcon class="button__icon"/>
                    <span class="button__text">View Projects</span>
                </NuxtLink>
                <a class="button" href="https://github.com/jacobtread" rel="noopener" target="_blank">
                    <GithubIcon class="button__icon"/>
                    <span class="button__text">View Github</span>
                </a>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";


.content {
    background: linear-gradient($first-block-tint-top, $first-block-tint-bottom);


    &--background {
        background: linear-gradient($first-gradient-top, $first-gradient-bottom);
    }

    &__title {
        background: $first-block-title-bg;
    }

    &__body {

        &__item__title__prefix {
            color: $first-block-subtitle-hash;
        }
    }
}

.button {
    background: $first-button-background;
}

</style>