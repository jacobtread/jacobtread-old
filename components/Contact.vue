<script setup lang="ts">
import InstagramIcon from "assets/icons/socials/instagram.svg?component"
import GithubIcon from "assets/icons/tech/github.svg?component"
import EmailIcon from "assets/icons/socials/mail.svg?component"
import DiscordIcon from "assets/icons/socials/discord.svg?component"

</script>
<template>
    <div class="content--background">
        <div class="content" id="contact">
            <a class="content__title" href="#contact">Contacting me</a>
            <div class="content__body">
                <div class="content__body__item">
                    <p class="content__body__item__text">
                        If you are looking to get in touch with me to discuss the creation of a project you
                        should reach out to me via either Discord or Email if you simply just would like to
                        check out my existing projects you can head over to my Github which is where a majority
                        of my project sources are.
                    </p>
                </div>

            </div>
            <div class="button-group">
                <a class="button" href="https://instagram.com/jacobtread" rel="noopener">
                    <InstagramIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Instagram</span>
                        <span class="button__subtext">instagram.com/jacobtread</span>
                    </span>
                </a>
                <a class="button" href="https://github.com/jacobtread" rel="noopener">
                    <GithubIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Github</span>
                        <span class="button__subtext">github.com/jacobtread</span>
                    </span>
                </a>
                <a class="button" href="mailto:jacobtread@gmail.com" rel="noopener">
                    <EmailIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Email</span>
                        <span class="button__subtext">jacobtread@gmail.com</span>
                    </span>
                </a>
                <button class="button" rel="noopener">
                    <DiscordIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Discord</span>
                        <span class="button__subtext">Jacobtread#3770</span>
                    </span>
                </button>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";


.content {
    background: linear-gradient($second-block-tint-top, $second-block-tint-bottom);


    &--background {
        background: linear-gradient($second-gradient-top, $second-gradient-bottom);
    }

    &__title {
        background: $second-block-title-bg;
    }

    &__body {

    }
}

.button-group {
    flex-flow: column;
}

.button {
    background: $second-button-background;

    &__icon {
        width: 48px;
    }

    &__content {
        display: flex;
        flex-flow: column;
        gap: 0.5rem;
    }

    &__subtext {
        color: $text;
    }
}

</style>