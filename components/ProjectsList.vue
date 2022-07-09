<script lang="ts" setup>
// Importing icon components to use as project icons
import GithubIcon from "./icons/GithubIcon.vue"
import QRLSIcon from "./icons/QRLIcon.vue"
import NZGMIcon from "./icons/NZGMIcon.vue"
import PondIcon from "./icons/PondIcon.vue"
import StudentIcon from "./icons/StudentIcon.vue"
import QuizlerIcon from "./icons/QuizlerIcon.vue"
import TrueRandomIcon from "./icons/TRIcon.vue"

// Import the link type for type checking links
import type { Link } from "~/components/Project.vue"

/**
 * Creates a new link to a repository that is stored
 * on GitHub. Uses the GitHub icon as the link icon
 * and the default text is "GitHub"
 *
 * @param repository The GitHub repository this link references
 * @param text The text used for the link button
 */
function createGithubLink(repository: string, text: string = 'GitHub'): Link {
    return {
        // GitHub's repositories are stored at https://github.com/{USERNAME}/{REPOSITORY}
        link: `https://github.com/${repository}`,
        icon: GithubIcon,
        text,
    }
}

/**
 * Creates a new link to a website. With the default text being
 * "View Website". This function exists to remove the boilerplate
 * of creating the objects over and  over again
 *
 * @param link The url which this link points to
 * @param text The text used for the link button
 */
function createWebsiteLink(link: string, text: string = 'View Website'): Link {
    return {link, text}
}

</script>
<template>
    <div class="content--background">
        <div id="projects" class="content">
            <div class="content__body">
                <Project
                        :icon="QRLSIcon"
                        :links="[
                            createGithubLink('jacobtread/QRLS'),
                            createGithubLink('jacobtread/QRLS-v2', 'V2 Github'),
                        ]"
                        :tags="['VueJS', 'SASS', 'TypeScript', 'JavaScript', 'HTML', 'NodeJS']"
                        name="QRLS"
                >
                    QRLS is a kiosk system for the Questionable Research Labs which allows members and guests
                    to sign in when entering the building and also manage and view who has been in the building.
                    There has been multiple iterations of this website first of which was not created by me but
                    since then there has been two new remakes by me.
                </Project>
                <Project
                        :icon="NZGMIcon"
                        :links="[
                            createGithubLink('jacobtread/NZGM'),
                            createWebsiteLink('https://grapher.jacobtread.com/'),
                            createWebsiteLink('https://grapher.nz/', 'NZGrapher'),
                        ]"
                        :tags="['VueJS', 'SASS', 'TypeScript']"
                        name="NZGM"
                >
                    NZGM (NZGrapher Modern) is a modern alternative to the NZGrapher web graphing application
                    which has many improvements of NZGrapher such as live editing data and the ability to run offline.
                </Project>
                <Project
                        :icon="PondIcon"
                        :links="[createGithubLink('jacobtread/Pond')]"
                        :tags="['Kotlin', 'Java', 'Flex (Lexer)']"
                        name="Pond">
                    Pond is a custom scripting language for writing scripts for a USB Rubber ducky it improves a
                    lot upon the existing ducky code language providing variables and macros.
                </Project>
                <Project
                        :icon="StudentIcon"
                        :links="[createGithubLink('jacobtread/KNI')]"
                        :tags="['Python', 'Java', 'PHP', 'Javascript', 'Kotlin', 'Rust', 'Typescript', '.NET']"
                        name="KNI">
                    KNI (KAMAR Notices Interface) is a collection of libraries in different programming languages
                    that all have the one purpose of fetching notices from the KAMAR portal application.
                </Project>
                <Project
                        :icon="StudentIcon"
                        :links="[createGithubLink('jacobtread/KJP')]"
                        :tags="['Go', 'JSON']"
                        name="KJP">
                    KJP (KAMAR JSON Pass-through) is a server written in Go which provides a way to connect to
                    and use KAMAR portal APIs through the web with easy to use JSON REST API
                </Project>
                <Project
                        :icon="StudentIcon"
                        :links="[createGithubLink('jacobtread/KPM')]"
                        :tags="['VueJS', 'SASS', 'Typescript']"
                        name="KPM">
                    KPM (KAMAR Portal Modern) An unfinished custom KAMAR portal web interface that uses more modern
                    technologies it runs all in the browser using a SPA and accesses KAMAR through KJP
                </Project>
                <Project
                        :icon="StudentIcon"
                        :links="[createGithubLink('jacobtread/KAMAR-Notices')]"
                        :tags="['PHP', 'HTML', 'CSS', 'Laravel']"
                        name="KAMAR-Notices">
                    A web application for pulling notices from KAMAR and displaying them in a nice easy to read view
                    that will cache results from KAMAR. Retrieves notices from KAMAR API using a PHP backend.
                </Project>
                <Project
                        :icon="StudentIcon"
                        :links="[createGithubLink('jacobtread/KAMAR2')]"
                        :tags="['Kotlin','Android','Jetpack Compose','XML','JSON']"
                        name="KAMAR2">
                    KAMAR2 is a very early unfinished project which aims to provide an open source alternative
                    to the KAMAR android app however its in a very early state.
                </Project>
                <Project
                        :icon="QuizlerIcon"
                        :links="[
                            createGithubLink('jacobtread/Quizler'),
                            createGithubLink('jacobtread/Quizler-rust', 'Rust Re-write'),
                            createWebsiteLink('https://quizler.jacobtread.com/'),
                        ]"
                        :tags="['VueJS', 'Typescript', 'Go', 'Rust']"
                        name="Quizler">
                    KAMAR2 is a very early unfinished project which aims to provide an open source alternative
                    to the KAMAR android app however its in a very early state.
                </Project>
                <Project
                        :icon="TrueRandomIcon"
                        :links="[
                            createGithubLink('Questionable-Research-Labs/TrueRandom-MainServer'),
                            createWebsiteLink('https://tr.host.qrl.nz/'),
                        ]"
                        :tags="['Typescript', 'HTML', 'SASS', 'NodeJS', 'ExpressJS']"
                        name="TrueRandom">
                    A joke website designed for a Hackathon. Centered around a dice rolling machine
                    as a service. For generating random numbers by a physically rolled dice
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/KME3')]"
                        :tags="['Kotlin', 'Mass Effect 3', 'Game Server', 'Netty', 'VueJS', 'SASS', 'Typescript']"
                        name="KME3">
                    A custom game server for Mass Effect 3 which emulates the functionality of the official
                    EA servers but allows home hosting or lan play and editing of player data. Also features
                    a MITM (Man-in-the-middle) functionality for connecting to the official servers and
                    logging the packets.
                </Project>
                <Project
                        :links="[createWebsiteLink('https://dreamclient.xyz/')]"
                        :tags="['VueJS', 'PHP', 'SASS', 'Typescript', 'Laravel']"
                        name="Dream"
                >
                    Dream is a WEB-GUI Minecraft Cheat that is controlled via your web browser and can be access from
                    any device that can use a web browser its written in VueJS with a PHP backend
                </Project>
                <Project
                        :links="[
                            createGithubLink('AltoClient'),
                            createWebsiteLink('https://alto.jacobtread.com/'),
                        ]"
                        :tags="['Kotlin', 'Java', 'VueJS', 'Minecraft', 'Go', 'OpenGL']"
                        name="Alto"
                >
                    Alto is a high performance Minecraft client written in Kotlin which greatly out performs
                    many clients available today. This project is pending rewrite
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/Hour.ly')]"
                        :tags="['Javascript', 'CSS', 'HTML', 'Electron']"
                        name="Hour.ly">
                    A small desktop electron app for keeping track of how many hours you've worked for.
                    Stores the information in a JSON file and displays a small counter in the corner of your screen.
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/MalDuino-W')]"
                        :tags="['Svelte', 'C++', 'Typescript', 'Javascript', 'SCSS', 'ESP8266', 'WebSocket', 'Arduino']"
                        name="Malduino-W Firmware">
                    A custom fork of the Malduino Wireless Bad-USB firmware with a more modern embedded
                    website which has a nice SPA which uses the Svelte frontend framework
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/DuckCentral')]"
                        :tags="['Kotlin', 'C++', 'Android', 'Jetpack Compose', 'ESP8266', 'WebSocket', 'Ardunio']"
                        name="DuckCentral">
                    An app for controlling the Malduino Wireless Bad-USB using a Android app with a
                    lightweight firmware that removes the embedded website for extra space.
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/TetriVersal')]"
                        :tags="['Typescript', 'Shell', 'NodeJS']"
                        name="TetriVersal">
                    An unfinished game of multiplayer tetris intended for use as the game for a school project.
                    Although unfinished it is completely playable it is only unfinished in terms of not having
                    a proper client completed the only way to play is through the testing client which is a terminal
                    client
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/InstaViewer')]"
                        :tags="['Java', 'Android']"
                        name="InstaViewer">
                    A simple app for viewing the full message contents of Instagram without opening actual direct
                    message.
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/Freddys-Fast-Food')]"
                        :tags="['Java', 'Android', 'Assessment']"
                        name="Freddy's Fast Food">
                    A python application submitted for an internal assessment in Digital Technologies for Achievement
                    Standard 91896.
                    A advanced ordering system written in python
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/Computron')]"
                        :tags="['VueJS', 'SCSS', 'Javascript', 'Website', 'Assessment']"
                        name="Computron">
                    A website designed, built and submitted for an internal assessment in Digital Technologies
                    for "Web Design 2.4 AS91893".
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/spew')]"
                        :tags="['Rust', 'Language']"
                        name="Spew">
                    A very early stages custom language the linked repository is the parser which is written in rust.
                </Project>
                <Project
                        :links="[createGithubLink('jacobtread/spew')]"
                        :tags="['VueJS', 'NuxtJS', 'Typescript']"
                        name="jacobtread.com">
                    The website you are currently on :). This is my personal website used to display information about
                    myself as well as a list of my projects, tech, and skills.
                </Project>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@import "assets/scss/colors";
@import "assets/scss/mixins";


.content {

  // To display the two rows properly on larger screens the
  // max width of this element is increased to 1200px from 900px
  max-width: 1200px;

  // Due to the large size of this single content block used for displaying
  // projects rather than having individual split sections with their own
  // gradients this uses a combination gradient of all the other gradients
  background: linear-gradient(
                  $first-block-tint-top, $first-block-tint-bottom,
                  $second-block-tint-top, $second-block-tint-bottom,
                  $third-block-tint-top, $third-block-tint-bottom,
  );

  // Logic for when the page becomes <= to 1200px
  @include max-width(1200px) {
    // Use the original max-width of 900px
    max-width: 900px;

    .content__body {
      // Reduce the number of columns to a single column this is
      // to better represent the list on smaller screens
      grid-template-columns: 1fr;
    }
  }

  &--background {
    // The previously mentioned gradient is also applied here
    background: linear-gradient(
                    $first-gradient-top, $first-gradient-bottom,
                    $second-gradient-top, $second-gradient-bottom,
                    $third-gradient-top, $third-gradient-bottom
    );
  }

  &__title {
    background: $first-block-title-bg;
  }

  &__body {
    gap: 3rem;
    display: grid;
    grid-template-columns: 1fr 1fr;

    &__item__title__prefix {
      color: $first-block-subtitle-hash;
    }
  }
}

.button {
  background: $first-button-background;
}
</style>