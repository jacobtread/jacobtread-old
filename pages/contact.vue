<script setup lang="ts">

import HLeft from "assets/img/hleft.svg?component";

import DiscordIcon from "assets/icons/socials/discord.svg?component"
import InstagramIcon from "assets/icons/socials/instagram.svg?component"
import MailIcon from "assets/icons/socials/mail.svg?component"
import SnapchatIcon from "assets/icons/socials/snapchat.svg?component"
import GitHubIcon from "assets/icons/tech/github.svg?component"

interface Contact {
    icon: any,
    name: string,
    text: string,
    link?: string
}

const contacts: Contact[] = [
    {icon: InstagramIcon, name: 'Instagram', text: 'Jacobtread', link: 'https://instagram.com/jacobtread'},
    {
        icon: SnapchatIcon,
        name: 'Snapchat',
        text: 'jacobtread',
        link: 'https://www.snapchat.com/add/jacobtread?share_id=m55FKairH1s&locale=en-NZ'
    },
    {icon: GitHubIcon, name: 'GitHub', text: 'jacobtread', link: 'https://github.com/jacobtread'},
    {icon: DiscordIcon, name: 'Discord', text: 'Jacobtread#3770'},
    {icon: MailIcon, name: 'Email', text: 'jacobtread@gmail.com', link: 'mailto:jacobtread@gmail.com'},
]

</script>
<template>
    <div>
        <HLeft class="graphic graphic--left"/>
        <div class="content">
            <Heading text="Home" link="/"/>
            <div class="block">
                <h1 class="block__title">Contacts</h1>
                <p class="block__text">This page contains all my available contact information</p>
                <div class="contacts">
                    <a v-for="contact in contacts" class="contact" :href="contact.link || '#'" target="_blank"
                       rel="noopener">
                        <component :is="contact.icon" class="contact__icon"></component>
                        <div class="contact__content">
                            <h2 class="contact__name">{{ contact.name }}</h2>
                            <p class="contact__text">{{ contact.text }}</p>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/variables";
@import "assets/scss/mixins";

.content {
  max-width: 1000px;
  margin: 1rem auto;
}

.graphic {
  position: absolute;
  z-index: -1;
  max-width: 100%;
  height: 100%;

  &--left {
    left: 0;
    top: 0;
  }
}

.contacts {
  display: flex;
  flex-flow: column;
  gap: 1rem;
}

.contact {
  display: flex;
  flex-flow: row;
  gap: 1rem;
  text-decoration: none;
  border: 3px solid $background-light;
  padding: 1rem;

  &__icon {
    width: 48px;
    height: 48px;
  }

  &__content {
    display: flex;
    flex-flow: column;
    gap: 0.5rem;
    text-align: left;
  }

  &__name {
    color: white;
    font-weight: bold;
  }

  &__text {
    color: $text-color;

  }
}
</style>