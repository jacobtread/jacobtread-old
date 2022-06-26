<script setup lang="ts">

interface Link {
    link: string
    text: string
    icon: any
}

interface Properties {
    icon: any,
    name: string,
    tags: string[] | undefined,
    links: Link[] | undefined
}

const { icon, name, tags, links } = defineProps<Properties>()

</script>
<template>
    <div class="content__body__item">
        <h2 class="content__body__item__title">
            <component v-if="icon" :is="icon" class="icon"/>
            <span>{{ name }}</span>
        </h2>
        <p class="content__body__item__text">
            <slot/>
        </p>
        <div class="button-group">
            <a v-for="link in links" class="button" :href="link.link" rel="noopener" target="_blank">
                <component v-if="link.icon" :is="link.icon" class="button__icon"/>
                <span class="button__text">{{ link.text }}</span>
            </a>
        </div>
        <div class="tags">
            <span class="tags__value" v-for="tag in tags">
                {{ tag }}
            </span>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";

.content__body__item__title {
    display: flex;
    align-items: center;
    gap: 1rem;
}

.button-group {
    margin: 1rem 0;
}

.icon {
    height: 32px;
    max-height: 32px;
    display: inline;
}

.tags {
    display: flex;
    flex-flow: row;
    gap: 1rem;

    &__value {
        padding: 0.5rem;
        background: $first-button-background;
        border-radius: 8px;
        color: $text;
        opacity: 0.5;

    }
}

</style>