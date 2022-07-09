<script setup lang="ts">
import GithubIcon from "./icons/GithubIcon.vue"
import QRLSIcon from "./icons/QRLIcon.vue"
import NZGMIcon from "./icons/NZGMIcon.vue"
import PondIcon from "./icons/PondIcon.vue"
import StudentIcon from "./icons/StudentIcon.vue"
import QuizlerIcon from "./icons/QuizlerIcon.vue"
import TrueRandomIcon from "./icons/TRIcon.vue"

</script>
<template>
    <div class="content--background">
        <div class="content" id="projects">
            <div class="content__body">
                <Project
                        :icon="QRLSIcon"
                        name="QRLS"
                        :tags="['VueJS', 'SASS', 'TypeScript', 'JavaScript', 'HTML', 'NodeJS']"
                        :links="[
                        {link:'https://github.com/jacobtread/QRLS', text: 'Github', icon: GithubIcon},
                        {link:'https://github.com/jacobtread/QRLS-v2', text: 'V2 Github', icon: GithubIcon},
                    ]">
                    QRLS is a kiosk system for the Questionable Research Labs which allows members and guests
                    to sign in when entering the building and also manage and view who has been in the building.
                    There has been multiple iterations of this website first of which was not created by me but
                    since then there has been two new remakes by me.
                </Project>
                <Project
                        :icon="NZGMIcon"
                        name="NZGM"
                        :tags="['VueJS', 'SASS', 'TypeScript']"
                        :links="[
                        {link:'https://github.com/jacobtread/NZGM', text: 'Github', icon: GithubIcon},
                        {link:'https://jacobtread.github.io/NZGM/', text: 'View Website'},
                        {link:'https://grapher.nz/', text: 'NZGrapher'},
                    ]">
                    NZGM (NZGrapher Modern) is a modern alternative to the NZGrapher web graphing application
                    which has many improvements of NZGrapher such as live editing data and the ability to run offline.
                </Project>
                <Project
                        :icon="PondIcon"
                        name="Pond"
                        :tags="['Kotlin', 'Java', 'Flex (Lexer)']"
                        :links="[{link:'https://github.com/jacobtread/Pond', text: 'Github', icon: GithubIcon}]">
                    Pond is a custom scripting language for writing scripts for a USB Rubber ducky it improves a
                    lot upon the existing ducky code language providing variables and macros.
                </Project>
                <Project
                        :icon="StudentIcon"
                        name="KNI"
                        :tags="['Python', 'Java', 'PHP', 'Javascript', 'Kotlin', 'Rust', 'Typescript', '.NET']"
                        :links="[{link:'https://github.com/jacobtread/KNI', text: 'Github', icon: GithubIcon}]">
                    KNI (KAMAR Notices Interface) is a collection of libraries in different programming languages
                    that all have the one purpose of fetching notices from the KAMAR portal application.
                </Project>
                <Project
                        :icon="StudentIcon"
                        name="KJP"
                        :tags="['Go', 'JSON']"
                        :links="[{link:'https://github.com/jacobtread/KJP', text: 'Github', icon: GithubIcon}]">
                    KJP (KAMAR JSON Pass-through) is a server written in Go which provides a way to connect to
                    and use KAMAR portal APIs through the web with easy to use JSON REST API
                </Project>
                <Project
                        :icon="StudentIcon"
                        name="KPM"
                        :tags="['VueJS', 'SASS', 'Typescript']"
                        :links="[{link:'https://github.com/jacobtread/KPM', text: 'Github', icon: GithubIcon}]">
                    KPM (KAMAR Portal Modern) An unfinished custom KAMAR portal web interface that uses more modern
                    technologies it runs all in the browser using a SPA and accesses KAMAR through KJP
                </Project>
                <Project
                        :icon="StudentIcon"
                        name="KAMAR-Notices"
                        :tags="['PHP', 'HTML', 'CSS', 'Laravel']"
                        :links="[{link:'https://github.com/jacobtread/KAMAR-Notices', text: 'Github', icon: GithubIcon}]">
                    A web application for pulling notices from KAMAR and displaying them in a nice easy to read view
                    that will cache results from KAMAR. Retrieves notices from KAMAR API using a PHP backend.
                </Project>
                <Project
                        :icon="StudentIcon"
                        name="KAMAR2"
                        :tags="['Kotlin','Android','Jetpack Compose','XML','JSON']"
                        :links="[{link:'https://github.com/jacobtread/KAMAR2', text: 'Github', icon: GithubIcon}]">
                    KAMAR2 is a very early unfinished project which aims to provide an open source alternative
                    to the KAMAR android app however its in a very early state.
                </Project>
                <Project
                        :icon="QuizlerIcon"
                        name="Quizler"
                        :tags="['VueJS', 'Typescript', 'Go', 'Rust']"
                        :links="[
                        {link:'https://github.com/jacobtread/Quizler', text: 'Github', icon: GithubIcon},
                        {link:'https://github.com/jacobtread/Quizler-rust', text: 'Rust Re-write', icon: GithubIcon},
                        {link:'https://quizler.jacobtread.com/', text: 'View Website'},
                    ]">
                    KAMAR2 is a very early unfinished project which aims to provide an open source alternative
                    to the KAMAR android app however its in a very early state.
                </Project>
                <Project
                        :icon="TrueRandomIcon"
                        name="TrueRandom"
                        :tags="['Typescript', 'HTML', 'SASS', 'NodeJS', 'ExpressJS']"
                        :links="[
                        {link:'https://github.com/Questionable-Research-Labs/TrueRandom-MainServer', text: 'Github', icon: GithubIcon},
                        {link:'https://tr.host.qrl.nz/', text: 'View Website'},
                    ]">
                    A joke website designed for a Hackathon. Centered around a dice rolling machine
                    as a service. For generating random numbers by a physically rolled dice
                </Project>
                <Project
                        name="KME3"
                        :tags="['Kotlin', 'Mass Effect 3', 'Game Server', 'Netty', 'VueJS', 'SASS', 'Typescript']"
                        :links="[{link:'https://github.com/jacobtread/KME3', text: 'Github', icon: GithubIcon}]">
                    A custom game server for Mass Effect 3 which emulates the functionality of the official
                    EA servers but allows home hosting or lan play and editing of player data. Also features
                    a MITM (Man in the middle) functionality for connecting to the official servers and
                    logging the packets.
                </Project>
                <Project
                        name="Dream"
                        :tags="['VueJS', 'PHP', 'SASS', 'Typescript', 'Laravel']"
                        :links="[
                        {link:'https://dreamclient.xyz/', text: 'View Website'},
                    ]">
                    Dream is a WEB-GUI Minecraft Cheat that is controlled via your web browser and can be access from
                    any
                    device that can use a web browser its written in VueJS with a PHP backend
                </Project>
                <Project
                        name="Alto"
                        :tags="['Kotlin', 'Java', 'VueJS', 'Minecraft', 'Go', 'OpenGL']"
                        :links="[
                        {link:'https://github.com/AltoClient', text: 'Github', icon: GithubIcon},
                        {link:'https://alto.jacobtread.com/', text: 'View Website'},
                    ]">
                    Alto is a high performance Minecraft client written in Kotlin which greatly out performs
                    many clients available today. This project is pending rewrite
                </Project>
                <Project
                        name="Hour.ly"
                        :tags="['Javascript', 'CSS', 'HTML', 'Electron']"
                        :links="[
                        {link:'https://github.com/jacobtread/Hour.ly', text: 'Github', icon: GithubIcon},
                    ]">
                    A small desktop electron app for keeping track of how many hours you've worked for.
                    Stores the information in a JSON file and displays a small counter in the corner of your screen.
                </Project>
                <Project
                        name="Malduino-W Firmware"
                        :tags="['Svelte', 'C++', 'Typescript', 'Javascript', 'SCSS', 'ESP8266', 'WebSocket', 'Arduino']"
                        :links="[{link:'https://github.com/jacobtread/MalDuino-W', text: 'Github', icon: GithubIcon}]">
                    A custom fork of the Malduino Wireless Bad-USB firmware with a more modern embedded
                    website which has a nice SPA which uses the Svelte frontend framework
                </Project>
                <Project
                        name="DuckCentral"
                        :tags="['Kotlin', 'C++', 'Android', 'Jetpack Compose', 'ESP8266', 'WebSocket', 'Ardunio']"
                        :links="[{link:'https://github.com/jacobtread/DuckCentral', text: 'Github', icon: GithubIcon}]">
                    An app for controlling the Malduino Wireless Bad-USB using a Android app with a
                    lightweight firmware that removes the embedded website for extra space.
                </Project>
                <Project
                        name="TetriVersal"
                        :tags="['Typescript', 'Shell', 'NodeJS']"
                        :links="[{link:'https://github.com/jacobtread/TetriVersal', text: 'Github', icon: GithubIcon}]">
                    An unfinished game of multiplayer tetris intended for use as the game for a school project.
                    Although unfinished it is completely playable it is only unfinished in terms of not having
                    a proper client completed the only way to play is through the testing client which is a terminal
                    client
                </Project>
                <Project
                        name="InstaViewer"
                        :tags="['Java', 'Android']"
                        :links="[{link:'https://github.com/jacobtread/InstaViewer', text: 'Github', icon: GithubIcon}]">
                    A simple app for viewing the full message contents of Instagram without opening actual direct
                    message.
                </Project>
                <Project
                        name="Freddy's Fast Food"
                        :tags="['Java', 'Android', 'Assessment']"
                        :links="[{link:'https://github.com/jacobtread/Freddys-Fast-Food', text: 'Github', icon: GithubIcon}]">
                    A python application submitted for an internal assessment in Digital Technologies for Achievement
                    Standard 91896.
                    A advanced ordering system written in python
                </Project>
                <Project
                        name="Computron"
                        :tags="['VueJS', 'SCSS', 'Javascript', 'Website', 'Assessment']"
                        :links="[{link:'https://github.com/jacobtread/Computron', text: 'Github', icon: GithubIcon}]">
                    A website designed, built and submitted for an internal assessment in Digital Technologies
                    for "Web Design 2.4 AS91893".
                </Project>
                <Project
                        name="Spew"
                        :tags="['Rust', 'Language']"
                        :links="[{link:'https://github.com/jacobtread/spew', text: 'Github', icon: GithubIcon}]">
                    A very early stages custom language the linked repository is the parser which is written in rust.
                </Project>
                <Project
                        name="jacobtread.com"
                        :tags="['VueJS', 'NuxtJS', 'Typescript']"
                        :links="[{link:'https://github.com/jacobtread/jacobtread.com', text: 'Github', icon: GithubIcon}]">
                    The website you are currently on :). This is my personal website used to display information about
                    myself as well as a list of my projects, tech, and skills.
                </Project>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
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