<script setup lang="ts">
import LinkIcon from "assets/icons/link.svg?component"
import GithubIcon from "assets/icons/tech/github.svg?component"
import ProjectsList from "~/components/ProjectsList.vue"
</script>
<template>
    <div>
        <Heading/>
        <main class="main">
            <div class="content">
                <div class="button-group">
                    <NuxtLink class="button" to="/">
                        <LinkIcon class="button__icon"/>
                        <span class="button__text">Back</span>
                    </NuxtLink>
                    <NuxtLink class="button" to="https://github.com/jacobtread" target="_blank">
                        <GithubIcon class="button__icon"/>
                        <span class="button__text">View Github</span>
                    </NuxtLink>
                </div>
            </div>
            <ProjectsList/>
        </main>
    </div>
</template>
<style lang="scss" scoped>
.button-group {
  flex-wrap: wrap;
}
</style>