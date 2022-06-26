<script setup lang="ts">

import LinkIcon from "assets/icons/link.svg?component"
import GithubIcon from "assets/icons/tech/github.svg?component"
import QRLSIcon from "assets/icons/projects/qrl.svg?component"</script>
<template>
    <div class="content--background">
        <div class="content" id="projects">
            <div class="content__body">
                <Project
                    :icon="QRLSIcon"
                    name="QRLS"
                    :tags="['VueJS', 'SASS', 'TypeScript', 'JavaScript', 'HTML', 'PHP']"
                    :links="[
                        {
                            link:'https://github.com/jacobtread/QRLS',
                            text: 'Github',
                            icon: GithubIcon
                        },
                         {
                            link:'https://github.com/jacobtread/QRLS-v2',
                            text: 'V2 Github',
                            icon: GithubIcon
                        },
                    ]"
                >
                    QRLS is a kiosk system for the Questionable Research Labs which allows members and guests
                    to sign in when entering the building and also manage and view who has been in the building.
                    There has been multiple iterations of this website first of which was not created by me but
                    since then there has been two new remakes by me.
                </Project>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";


.content {
    background: linear-gradient($first-block-tint-top, $first-block-tint-bottom);


    &--background {
        background: linear-gradient($first-gradient-top, $first-gradient-bottom);
    }

    &__title {
        background: $first-block-title-bg;
    }

    &__body {

        &__item__title__prefix {
            color: $first-block-subtitle-hash;
        }
    }
}

.button {
    background: $first-button-background;
}

</style>