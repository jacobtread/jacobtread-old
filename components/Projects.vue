<script setup lang="ts">
import QRLIcon from "assets/icons/projects/qrl.svg?component"
import NZGMIcon from "assets/icons/projects/nzgm.svg?component"
import PondIcon from "assets/icons/projects/pond.svg?component"
import KNIIcon from "assets/icons/projects/kni.svg?component"
import QuizlerIcon from "assets/icons/projects/quizler.svg?component"
import TrueRandomIcon from "assets/icons/projects/tr.svg?component"
import GitHubIcon from "@/assets/icons/tech/github.svg?component";

const link = (link: string, text: string = 'View Website'): ProjectLink => ({link, text})
const githubLink = (link: string, text: string = 'Github'): ProjectLink => ({link, text, icon: GitHubIcon,})

interface ProjectLink {
    text: string,
    link: string,
    icon?: any,
}

interface Project {
    name: string,
    description: string,
    links?: ProjectLink[],
    icon?: any,
    tags?: string[],
}

const projects: Project[] = [
    {
        name: 'QRLS',
        description: 'QRLS is a kiosk system for the Questionable Research Labs which allows members and guests to sign in when entering the building and also manage and view who has been in the building.',
        icon: QRLIcon,
        links: [
            githubLink('jacobtread/QRLS'),
            githubLink('jacobtread/QRLS-v2', 'v2 GitHub')
        ],
        tags: ['VueJS', 'SASS', 'TypeScript', 'JavaScript', 'HTML']
    },
    {
        name: 'NZGM',
        description: 'NZGM (NZGrapher Modern) is a modern alternative to the NZGrapher web graphing application which has many improvements of NZGrapher such as live editing data and the ability to run offline.',
        icon: NZGMIcon,
        links: [
            githubLink('jacobtread/NZGM'),
            link('https://jacobtread.github.io/NZGM/'),
            link('https://grapher.nz', 'NZGrapher'),
        ],
        tags: ['VueJS', 'SASS', 'TypeScript']
    },
    {
        name: 'Pond',
        description: 'Pond is a custom scripting language for writing scripts for a USB Rubber ducky it improves a lot upon the existing ducky code language providing variables and macros.',
        icon: PondIcon,
        links: [githubLink('jacobtread/Pond')],
        tags: ['Kotlin', 'Java', 'Flex (Lexer)']
    },
    {
        name: 'KNI',
        description: 'KNI (KAMAR Notices Interface) is a collection of libraries in different programming languages that all have the one purpose of fetching notices from the KAMAR portal application.',
        icon: KNIIcon,
        links: [githubLink('jacobtread/KNI')],
        tags: ['Python', 'Java', 'PHP', 'Javascript', 'Kotlin', 'Rust', 'Typescript', '.NET']
    },
    {
        name: 'KJP',
        description: 'KJP (KAMAR JSON Pass-through) is a server written in Go which provides a way to connect to and use KAMAR portal APIs through the web with easy to use JSON REST API',
        icon: KNIIcon,
        links: [githubLink('jacobtread/KJP')],
        tags: ['Go']
    },
    {
        name: 'KPM',
        description: 'KPM (KAMAR Portal Modern) An unfinished custom KAMAR portal web interface that uses more modern technologies it runs all in the browser using a SPA and accesses KAMAR through KJP',
        icon: KNIIcon,
        links: [githubLink('jacobtread/KPM')],
        tags: ['VueJS', 'SASS', 'TypeScript']
    },
    {
        name: 'KAMAR-Notices',
        description: 'A web application for pulling notices from KAMAR and displaying them in a nice easy to read view that will cache results from KAMAR. Retreives notices from KAMAR API using a PHP backend.',
        icon: KNIIcon,
        links: [githubLink('jacobtread/KAMAR-Notices')],
        tags: ['PHP', 'HTML', 'CSS', 'Laravel']
    },
    {
        name: 'Quizler',
        description: 'A real time quiz application for quickly and easily making quizzes with an extremely small deployment size of 1.82mb making it extra portable. There is an in progress rewrite in the Rust language.',
        icon: QuizlerIcon,
        links: [
            githubLink('jacobtread/Quizler'),
            githubLink('jacobtread/Quizler-rust', 'Rust Rewrite'),
            link('https://quizler.jacobtread.com/')
        ],
        tags: ['VueJS', 'TypeScript', 'Go', 'Rust']
    },
    {
        name: "TrueRandom",
        description: 'A joke website designed for a Hackathon. Centered around a dice rolling machine as a service. For generating random numbers by a physically rolled dice',
        icon: TrueRandomIcon,
        links: [
            githubLink('Questionable-Research-Labs/TrueRandom-MainServer'),
            link('https://tr.host.qrl.nz/')
        ],
        tags: ['TypeScript', 'HTML', 'SASS', 'NodeJS']
    },
    {
        name: "Dream",
        description: 'Dream is a WEB-GUI Minecraft Cheat that is controlled via your web browser and can be access from any device that can use a web browser its written in VueJS with a PHP backend',
        links: [link('https://dreamclient.xyz/')],
        tags: ['VueJS', 'PHP', 'SASS', 'Typescript', 'Laravel']
    },
    {
        name: 'Alto',
        description: 'Alto is a high performance Minecraft client written in Kotlin which greatly out performs many clients available today. This project is pending rewrite',
        links: [
            githubLink('AltoClient'),
            link('https://alto.jacobtread.com/')
        ],
        tags: ['Kotlin', 'Java', 'VueJS', 'Minecraft']
    },
    {
        name: 'Hour.ly',
        description: 'A small desktop electron app for keeping track of how many hours you\'ve worked for. Stores the information in a JSON file and displays a small counter in the corner of your screen.',
        links: [githubLink('jacobtread/Hour.ly')],
        tags: ['JavaScript', 'CSS', 'HTML', 'Electron']
    },
    {
        name: 'Malduino-W Firmware',
        description: 'A custom fork of the Malduino Wireless Bad-USB firmware with a more modern embedded website which has a nice SPA which uses the Svelte frontend framework',
        links: [githubLink('jacobtread/MalDuino-W')],
        tags: ['Svelte', 'C++', 'TypeScript', 'JavaScript', 'SCSS', 'ESP8266']
    },
    {
        name: 'DuckCentral',
        description: 'An app for controlling the Malduino Wireless Bad-USB using a Android app with a lightweight firmware that removes the embedded website for extra space.',
        links: [githubLink('jacobtread/DuckCentral')],
        tags: ['Kotlin', 'C++', 'Android', 'Jetpack Compose']
    },
    {
        name: 'KME3',
        description: 'A custom game server for Mass Effect 3 which emulates the functionality of the official EA servers but allows home hosting or lan play and editing of player data',
        links: [githubLink('/jacobtread/KME3')],
        tags: ['Kotlin', 'Game Server']
    },
    {
        name: 'TetriVersal',
        description: 'An unfinished game of multiplayer tetris intended for use as the game for a school project. Although unfinished it is completely playable it is only unfinished in terms of not having a proper client completed the only way to play is through the testing client which is a terminal client',
        links: [githubLink('jacobtread/TetriVersal')],
        tags: ['TypeScript', 'Shell', 'NodeJS']
    },
    {
        name: 'InstaViewer',
        description: 'A simple app for viewing the full message contents of Instagram without opening actual direct message.',
        links: [githubLink('jacobtread/InstaViewer')],
        tags: ['Java', 'Android']
    },
    {
        name: 'Freddy\'s Fast Food',
        description: 'A python application submitted for an internal assessment in Digital Technologies for Achievement Standard 91896. A simple ordering system written in python',
        links: [githubLink('jacobtread/Freddys-Fast-Food')],
        tags: ['Python', 'School']
    }
];
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
                    <a class="project__links__item" v-for="link in project.links" :href="link.link">
                        <component v-if="link.icon" :is="link.icon" class="project__links__item__icon"/>
                        {{ link.text }}
                    </a>
                </div>
                <div v-if="project.tags" class="project__tags">
                    <span v-for="tag in project.tags" class="project__tags__item">{{ tag }}</span>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";

.projects {
  display: flex;
  flex-flow: column wrap;
  gap: 1rem;
}

.project {
  color: $text-color;
  padding: 1rem;
  border: 2px solid $background-light;
  text-align: left;

  transition: border-color 0.5s ease, transform 0.25s ease, background-color 0.25s ease;

  &__icon {
    display: inline;
    float: left;
    margin-right: 1rem;
    height: 32px;
    margin-bottom: 0.5rem;
    opacity: 0.5;
  }

  &__name {
    color: white;
    margin-bottom: 0.5rem;
    font-weight: bold;
  }

  &__desc {
    line-height: 1.5;
  }

  &__links {
    display: flex;
    flex-flow: row wrap;
    gap: 0.5rem;
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;

    &__item {
      padding: 0.5rem;
      background: $background-light;
      color: white;
      text-decoration: none;
      font-weight: bold;
      text-transform: uppercase;

      &__icon {
        width: 1em;
        height: 1em;
        vertical-align: middle;
      }
    }
  }

  &:hover {
    transform: perspective(500px) rotateX(5deg);
    border-bottom-color: $primary;
    background: $background-light;

    .project__tags__item, .project__links__item {
      background: $background;
    }
  }

  &__tags__item, &__links__item {
    transition: background-color 0.25s ease;
  }

  &__tags {
    display: flex;
    flex-flow: row wrap;
    gap: 0.5rem;
    margin-top: 0.5rem;
    align-items: stretch;

    &__item {
      font-size: 0.7em;
      background: $background-light;
      padding: 0.5rem;
    }
  }
}

</style>