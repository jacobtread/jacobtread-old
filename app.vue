<script setup lang="ts">

const TYPER_VALUES: string[] = [
    'Web', 'Kotlin', 'Stonks™',
    'JS', 'PHP', 'Go', 'Rust', 'Cool',
    'Bad', 'Cheat', 'HTML', 'CSS',
]

</script>
<template>
    <div class="heading">
        <img src="img/jacobtread.png" alt="" class="heading__logo">
        <div class="heading__content">
            <p class="heading__intro">
                Hey! my name is <span class="heading__intro__name">Jacobtread</span>
                <br>and im a
                <span class="heading__role">
                       <ClientOnly>
                    <Typer class="typer" :values="TYPER_VALUES" :duration="2000"/>
                </ClientOnly>
                <span class="heading__role__suffix">Developer</span>
                </span>
            </p>
            <Quote
                    text="when you don't create things, you become defined by your tastes rather than ability. your tastes only narrow & exclude people. so create."
                    author="Jonathan Gillette"
            />
        </div>
    </div>
    <div class="block">
        <h1 class="block__title">About me</h1>
        <p>
            
        </p>
    </div>
</template>
<style lang="scss">
@import "assets/scss/variables";
@import "assets/scss/mixins";

.heading {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 2rem;
  min-height: 100vh;

  &__logo {
    max-height: 300px;
  }

  &__content {
    text-align: center;
  }

  &__intro {
    line-height: 1.5;
    font-size: 1.5rem;
    color: $text-color;

    &__name {
      color: $primary;
      font-weight: bold;
    }
  }

  &__name {
    font-size: 2rem;
    margin-top: 1rem;
    color: $primary;
    font-weight: bold;
    text-align: center;
  }

  &__role {
    display: inline-block;
    background: $background-dark;
    padding: 0 0.5rem;
    font-size: 1.5rem;
    font-family: $font-family;
    font-weight: bold;

    .typer {
      color: $primary;
    }

    &__suffix {
      margin-left: 0.5rem;
      color: $text-color;
    }
  }

  @include max-width(900px) {
    flex-flow: column;
    gap: 4rem;
    padding: 2rem;
  }

}


</style>
