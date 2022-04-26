<script setup lang="ts">
import QRLIcon from "assets/icons/projects/qrl.svg?component"
import NZGMIcon from "assets/icons/projects/nzgm.svg?component"
import GitHubIcon from "@/assets/icons/tech/github.svg?component";

function flatten(value: string): string {
    return value.trim().replaceAll('\n', '')
}

function defaultLink(link: string): ProjectLink {
    return {
        link,
        text: 'View Website',
    }
}

function githubLink(link: string) {
    return {
        link,
        text: 'Github',
        icon: GitHubIcon,
    }
}

interface ProjectLink {
    text: string,
    link: string,
    icon?: any,
}

interface Project {
    name: string,
    description: string,
    links?: ProjectLink[],
    icon?: any
}

const projects: Project[] = [
    {
        name: 'QRLS',
        description: flatten(`
            QRLS is a kiosk system for the Questionable
            Research Labs which allows members and guests
            to sign in when entering the building and also
            manage and view who has been in the building.
        `),
        icon: QRLIcon,
        links: [githubLink('https://github.com/jacobtread/QRLS')]
    },
    {
        name: 'NZGM',
        description: flatten(`
             NZGM (NZGrapher Modern) is a modern alternative to
             the NZGrapher web graphing application which has
             many improvements of NZGrapher such as live editing
             data and the ability to run offline.
        `),
        icon: NZGMIcon,
        links: [
            githubLink('https://github.com/jacobtread/NZGM'),
            defaultLink('https://jacobtread.github.io/NZGM/'),
            {text: 'NZGrapher', link: 'https://grapher.nz/'}
        ]
    },
    {
        name: 'Pond',
        description: flatten(`
             Pond is a custom scripting language for writing scripts
             for a USB Rubber ducky it improves a lot upon the existing
             ducky code language providing variables and macros.
        `),

    }
]


</script>
<template>
    <div class="block">
        <h1 class="block__title">Projects</h1>
        <p class="block__text">
            Here's a list of projects that I've either completed or are currently ongoing
        </p>
        <div class="projects">
            <div v-for="project in projects" class="project">
                <component v-if="project.icon" :is="project.icon" class="project__icon"/>
                <h2 class="project__name">{{ project.name }}</h2>
                <p class="project__desc">{{ project.description }}</p>
                <div v-if="project.links" class="project__links">
                    <a class="project__link" v-for="link in project.links" :href="link.link">
                        <component v-if="link.icon" :is="link.icon" class="project__link__icon"/>
                        {{ link.text }}
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.projects {
  display: flex;
}

.project {
  &__icon {
    width: 32px;
    height: 32px;
  }

  &__link {
    &__icon {
      width: 1em;
      height: 1em;
      vertical-align: middle;
    }
  }
}

</style>