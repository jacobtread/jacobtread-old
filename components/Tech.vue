<script setup lang="ts">

</script>
<template>
    <div class="content--background">
        <div class="content" id="tech">
            <div class="content__split">
                <div class="content__split__img">
                    <img src="/img/langb.png" alt="Backend Languages">
                </div>
                <div class="content__split__body">
                    <h1 class="content__title">Backend Languages</h1>
                    <div class="content__body">
                        <div class="content__body__item">
                            <p class="content__body__item__text">
                                I am very familiar with languages such as Java and Kotlin having roughly 5 years experience programming with Java and
                                around 1 and a half years with kotlin. I’ve recently been getting into the mix of Rust and Go which have been a pleasure
                                to use. I also have 2 years experience in PHP.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="content__split">
                <div class="content__split__img">
                    <img src="/img/langf.png" alt="Frontend Languages">
                </div>
                <div class="content__split__body">
                    <h1 class="content__title">Frontend Languages</h1>
                    <div class="content__body">
                        <div class="content__body__item">
                            <p class="content__body__item__text">
                                I am very well accustomed to popular frontend languages like Javascript and Typescript with
                                around 4 years experienced in them both added up. I have been using them a lot throughout
                                many of my projects.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="content__split">
                <div class="content__split__img">
                    <img src="/img/editors.png" alt="IDE & Editors">
                </div>
                <div class="content__split__body">
                    <h1 class="content__title">IDE & Editors</h1>
                    <div class="content__body">
                        <div class="content__body__item">
                            <p class="content__body__item__text">
                                When it comes to IDE’s my platform of choice is the JetBrains collection of IDE’s i’ve grown
                                accustom to them and I am very comfortable using them and navigating them with ease.
                                For common every day text editing and some smaller projects I like to use VSCode.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="content__split">
                <div class="content__split__img">
                    <img src="/img/framb.png" alt="Backend Frameworks & Tooling">
                </div>
                <div class="content__split__body">
                    <h1 class="content__title">Backend Frameworks & Tooling</h1>
                    <div class="content__body">
                        <div class="content__body__item">
                            <p class="content__body__item__text">
                                I am very familiar with the Laravel php framework having shipped multiple production projects using it in the past. NuxtJS was the framework which I previously developed my personal website in among other side
                                projects. I have used NodeJS to make bots as well as other usefull tools and full on server systems.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="content__split">
                <div class="content__split__img">
                    <img src="/img/framf.png" alt="Frontend Frameworks & Tooling">
                </div>
                <div class="content__split__body">
                    <h1 class="content__title">Frontend Frameworks & Tooling</h1>
                    <div class="content__body">
                        <div class="content__body__item">
                            <p class="content__body__item__text">
                                I am quite familiar with a number of front-end frameworks my favorite of which is VueJS.
                                I have a few other assorted frameworks mixed in throughout my project but VueJS tends to
                                be the one I rely on the most.
                            </p>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";


.content {
    gap: 3rem;

    &__split {
        display: flex;
        flex-flow: row;
        gap: 2rem;
        align-items: stretch;

        &:nth-child(even) {
            flex-flow: row-reverse;
        }

        &__img {
            height: 100%
        }

        &__body {
            flex: auto;
            display: flex;
            flex-flow: column;
            gap: 1.5rem;
        }
    }

    background: linear-gradient($third-block-tint-top, $third-block-tint-bottom);


    &--background {
        background: linear-gradient($third-gradient-top, $third-gradient-bottom);
    }

    &__title {
        background: $third-block-title-bg;
    }
}

</style>