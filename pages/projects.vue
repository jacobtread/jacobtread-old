<script setup lang="ts">
import LinkIcon from "assets/icons/link.svg?component"
import GithubIcon from "assets/icons/tech/github.svg?component"
import ProjectsList from "~/components/ProjectsList.vue"
</script>
<template>
    <div>
        <HeadingProjects text="Contact" link="contact"/>
        <main class="main">
            <div class="content">
                <div class="button-group">
                    <NuxtLink class="button" to="/">
                        <LinkIcon class="button__icon"/>
                        <span class="button__text">Back</span>
                    </NuxtLink>
                    <a class="button" href="https://github.com/jacobtread" rel="noopener" target="_blank">
                        <GithubIcon class="button__icon"/>
                        <span class="button__text">View Github</span>
                    </a>
                </div>
            </div>
            <ProjectsList/>
        </main>
    </div>
</template>