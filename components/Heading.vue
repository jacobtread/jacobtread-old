<script setup lang="ts">
import LinkIcon from "assets/icons/link.svg?component";

interface Properties {
    link: string,
    text: string,
}

const {link, text} = defineProps<Properties>()

const TYPER_VALUES: string[] = [
    'Web', 'Kotlin', 'Stonks™',
    'JS', 'PHP', 'Go', 'Rust', 'Cool',
    'Bad', 'Cheat', 'HTML', 'CSS',
    '!Good',
]
</script>
<template>
    <div class="heading">
        <img src="/jacobtread.png" alt="" class="heading__logo">
        <div class="heading__content">
            <p class="heading__intro">
                My name is <span class="heading__intro__name">Jacobtread <span class="heading__intro__name__say">(Pronounced Jacob T Read)</span></span>
                and im a
                <span class="heading__role">
                    <ClientOnly>
                        <Typer class="typer" :values="TYPER_VALUES" :duration="2000"/>
                    </ClientOnly>
                    <span class="heading__role__suffix">Developer</span>
                </span>
            </p>
            <Quote
                    class="quote"
                    text="when you don't create things, you become defined by your tastes rather than ability. your tastes only narrow & exclude people. so create."
                    author="Jonathan Gillette"
            />
            <NuxtLink :to="link" rel="noopener" class="link">
                <LinkIcon class="link__icon"/>
                {{text}}
            </NuxtLink>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";
@import "assets/scss/mixins";

.link {
  cursor: pointer;
  background-color: $background-light;
  border-radius: 0.5rem;
  font-size: 1rem;
  font-weight: bold;
  color: white;
  padding: 0.5rem 1rem 0.5rem 0.5rem;
  display: inline-block;
  margin: 1rem 0 0.5rem;
  text-transform: uppercase;
  text-decoration: none;

  &__icon {
    width: 1.5rem;
    height: 1.5rem;
    vertical-align: middle;
  }
}

.heading {
  display: flex;
  flex-flow: row;
  justify-content: center;
  gap: 2rem;
  align-items: stretch;
  margin: 3rem 0;


  @include max-width(900px) {
    flex-flow: column;
    gap: 4rem;
  }


  &__logo {
    max-height: 300px;
    max-width: 300px;
    width: 100%;
    animation: logo 1s ease forwards;
    opacity: 0;
    align-self: center;
  }

  @keyframes logo {
    0% {
      opacity: 0;
      transform: scale(0);
    }
    100% {
      opacity: 1;
      transform: scale(1);
    }
  }

  &__content {
    border-left: 5px solid $primary-dark;
    background: $background-dark-op;
    padding: 2rem 2rem 1rem;
    opacity: 0;
    animation: content 1s 0.5s cubic-bezier(0, 0.9, 1, 1) forwards;

    @include max-width(900px) {
      text-align: center;
    }
  }

  @keyframes content {
    0% {
      opacity: 0;
      transform: translateX(-25%);
    }
    100% {
      opacity: 1;
      transform: translateX(0);
    }
  }

  &__intro {
    line-height: 1.5;
    font-size: 1.5rem;
    color: $text-color;
    opacity: 0.95;
    max-width: 600px;

    &__name {
      color: $primary;
      font-weight: bold;

      &__say {
        color: $text-color;
        opacity: 0.5;
        font-size: 0.95rem;
        vertical-align: middle;
      }
    }

    @media screen and (max-width: 640px) {
      .heading__intro__name__say {
        display: none;
      }
    }
  }


  &__name {
    font-size: 2rem;
    margin-top: 1rem;
    color: $primary;
    font-weight: bold;
  }

  &__role {
    display: inline-block;
    font-size: 1.5rem;
    font-weight: bold;

    .typer {
      color: $primary;
    }

    &__suffix {
      margin-left: 0.5rem;
      color: $text-color;
    }
  }
}
</style>