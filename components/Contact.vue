<script setup lang="ts">
import InstagramIcon from "~/components/icons/InstagramIcon.vue"
import GithubIcon from "~/components/icons/GithubIcon.vue"
import EmailIcon from "~/components/icons/MailIcon.vue"
import DiscordIcon from "~/components/icons/DiscordIcon.vue"

</script>
<template>
    <div class="content--background">
        <div class="content" id="contact">
            <NuxtLink class="content__title" to="#contact">Contacting me</NuxtLink>
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
                <NuxtLink class="button" to="https://instagram.com/jacobtread" target="_blank">
                    <InstagramIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Instagram</span>
                        <span class="button__subtext">instagram.com/jacobtread</span>
                    </span>
                </NuxtLink>
                <NuxtLink class="button" to="https://github.com/jacobtread" target="_blank">
                    <GithubIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Github</span>
                        <span class="button__subtext">github.com/jacobtread</span>
                    </span>
                </NuxtLink>
                <NuxtLink class="button" to="mailto:jacobtread@gmail.com" target="_blank">
                    <EmailIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Email</span>
                        <span class="button__subtext">jacobtread@gmail.com</span>
                    </span>
                </NuxtLink>
                <div class="button">
                    <DiscordIcon class="button__icon"/>
                    <span class="button__content">
                        <span class="button__text">Discord</span>
                        <span class="button__subtext">Jacobtread#3770</span>
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";
@import "assets/scss/mixins";


.content {
  background: linear-gradient($second-block-tint-top, $second-block-tint-bottom);


  &--background {
    background: linear-gradient($second-gradient-top, $second-gradient-bottom);
  }

  &__title {
    background: $second-block-title-bg;
  }
}

.button-group {
  flex-flow: column;

  @include max-width(430px) {
    flex-flow: row wrap;
    justify-content: center;
  }
}

.button {
  background: $second-button-background;
  @include max-width(430px) {
    justify-content: center;
  }

  &__icon {
    width: 48px;
  }

  &__content {
    display: flex;
    flex-flow: column;
    gap: 0.5rem;

    @include max-width(430px) {
      display: none;
    }
  }

  &__subtext {
    color: $text;
  }
}

</style>