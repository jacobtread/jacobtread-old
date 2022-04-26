<script setup lang="ts">
import QRLIcon from "assets/icons/projects/qrl.svg?component"
import NZGMIcon from "assets/icons/projects/nzgm.svg?component"
import PondIcon from "assets/icons/projects/pond.svg?component"
import KNIIcon from "assets/icons/projects/kni.svg?component"
import QuizlerIcon from "assets/icons/projects/quizler.svg?component"
import GitHubIcon from "@/assets/icons/tech/github.svg?component";
import VueIcon from "@/assets/icons/tech/vuejs.svg?component";
import SassIcon from "@/assets/icons/langs/sass.svg?component";
import TypescriptIcon from "@/assets/icons/langs/typescript.svg?component";
import JavascriptIcon from "@/assets/icons/langs/js.svg?component";
import KotlinIcon from "@/assets/icons/langs/kotlin.svg?component";
import JavaIcon from "@/assets/icons/langs/java.svg?component";
import PythonIcon from "@/assets/icons/langs/python.svg?component";
import PhpIcon from "@/assets/icons/langs/php.svg?component";

const flatten = (value: string) => value.trim().replaceAll('\n', '')
const link = (link: string, text: string = 'View Website'): ProjectLink => ({link, text: 'View Website'})
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
    languages?: any[],
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
        links: [
            githubLink('jacobtread/QRLS'),
            githubLink('jacobtread/QRLS-v2', 'v2 GitHub')
        ],
        languages: [VueIcon, SassIcon, TypescriptIcon, JavascriptIcon]
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
            githubLink('jacobtread/NZGM'),
            link('https://jacobtread.github.io/NZGM/'),
            link('https://grapher.nz', 'NZGrapher'),
        ],
        languages: [VueIcon, SassIcon, TypescriptIcon]
    },
    {
        name: 'Pond',
        description: flatten(`
             Pond is a custom scripting language for writing scripts
             for a USB Rubber ducky it improves a lot upon the existing
             ducky code language providing variables and macros.
        `),
        icon: PondIcon,
        links: [githubLink('jacobtread/Pond')],
        languages: [KotlinIcon, JavaIcon]
    },
    {
        name: 'KNI',
        description: flatten(`
             KNI (KAMAR Notices Interface) is a collection of libraries in
             different programming languages that all have the one purpose of
             fetching notices from the KAMAR portal application.
        `),
        icon: KNIIcon,
        links: [githubLink('jacobtread/KNI')],
        languages: [PythonIcon, JavaIcon, PhpIcon]
    },
    {
        name: 'KJP',
        description: flatten(`
              KJP (KAMAR JSON Pass-through) is a server written in Go which provides
              a way to connect to and use KAMAR portal APIs through the web with easy
              to use JSON REST API
        `),
        icon: KNIIcon,
        links: [githubLink('jacobtread/KJP')]
    },
    {
        name: 'KPM',
        description: flatten(`
              KPM (KAMAR Portal Modern) An unfinished custom KAMAR portal web interface
              that uses more modern technologies it runs all in the browser using a SPA
              and accesses KAMAR through KJP
        `),
        icon: KNIIcon,
        links: [githubLink('jacobtread/KPM')]
    },
    {
        name: 'KAMAR-Notices',
        description: flatten(`
              A web application for pulling notices from KAMAR and displaying them in a
              nice easy to read view that will cache results from KAMAR. Retreives notices
              from KAMAR API using a PHP backend.
        `),
        links: [githubLink('jacobtread/KAMAR-Notices')]
    },
    {
        name: "Dream",
        description: flatten(`
              Dream is a WEB-GUI Minecraft Cheat that is controlled via your web
              browser and can be access from any device that can use a web browser
              its written in VueJS with a PHP backend
        `),
        links: [link('https://dreamclient.xyz/')]
    },
    {
        name: "TrueRandom",
        description: flatten(`
              A joke website designed for a Hackathon. Centered around a dice rolling machine
              as a service. For generating random numbers by a physically rolled dice
        `),
        links: [
            githubLink('Questionable-Research-Labs/TrueRandom-MainServer'),
            link('https://tr.host.qrl.nz/')
        ]
    },
    {
        name: 'Alto',
        description: flatten(`
              Alto is a high performance Minecraft client written in Kotlin which greatly
              out performs many clients available today. This project is pending rewrite
        `),
        links: [
            githubLink('AltoClient'),
            link('https://alto.jacobtread.com/')
        ]
    },
    {
        name: 'Quizler',
        description: flatten(`
             A real time quiz application for quickly and easily making quizzes with an
             extremely small deployment size of 1.82mb making it extra portable . There
             is an in progress rewrite in the Rust language.
        `),
        icon: QuizlerIcon,
        links: [
            githubLink('jacobtread/Quizler'),
            githubLink('jacobtread/Quizler-rust', 'Rust Rewrite'),
            link('https://quizler.jacobtread.com/')
        ]
    },
    {
        name: 'Hour.ly',
        description: flatten(`
             A small desktop electron app for keeping track of how many hours you've
             worked for. Stores the information in a JSON file and displays a small
             counter in the corner of your screen.
        `),
        links: [githubLink('jacobtread/Hour.ly'),]
    },
    {
        name: 'Malduino-W Firmware',
        description: flatten(`
             A custom fork of the Malduino Wireless Bad-USB firmware with a more modern
             embedded website which has a nice SPA which uses the Svelte frontend framework
        `),
        links: [githubLink('jacobtread/MalDuino-W'),]
    },
    {
        name: 'DuckCentral',
        description: flatten(`
             An app for controlling the Malduino Wireless Bad-USB using a Android app with
             a lightweight firmware that removes the embedded website for extra space.
        `),
        links: [githubLink('jacobtread/DuckCentral'),]
    },
    {
        name: 'TetriVersal',
        description: flatten(`
             An unfinished game of multiplayer tetris intended for use as the game for a school
             project. Although unfinished it is completely playable it is only unfinished in terms
             of not having a proper client completed the only way to play is through the testing
             client which is a terminal client
        `),
        links: [githubLink('jacobtread/TetriVersal'),]
    },
    {
        name: 'InstaViewer',
        description: flatten(`
             A simple app for viewing the full message contents of Instagram without opening
             actual direct message.
        `),
        links: [githubLink('jacobtread/InstaViewer'),]
    },
    {
        name: 'Freddys Fast Food',
        description: flatten(`
             A python application submitted for an internal assessment in Digital Technologies
             for Achievement Standard 91896. A simple ordering system written in python
        `),
        links: [githubLink('jacobtread/Freddys-Fast-Food'),]
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
  flex-flow: row wrap;
}

.project {
  &__icon {
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