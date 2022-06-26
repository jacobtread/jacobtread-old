<script setup lang="ts">
const currentYear = new Date()
    .getFullYear()
</script>
<template>
    <div class="footer--background">
        <footer class="footer">
            <div class="footer--wrapper">
                <h1 class="footer__title">JR</h1>
                <p class="footer__mail">jacobtread@gmail.com</p>
                <p class="footer__subtitle">Copyright &copy; 2020 - {{ currentYear }} Jacobtread</p>
            </div>
        </footer>
    </div>
</template>
<style scoped lang="scss">
@import "assets/scss/colors";

.footer {
    background: $footer-background;
    color: white;
    padding: 2rem;

    &--wrapper {
        max-width: 900px;
        width: 100%;
        margin: 0 auto;
    }

    &--background {
        background: linear-gradient($footer-gradient-top, $footer-gradient-bottom);
        padding-top: 7rem;
    }

    &__title {
        font-size: 4rem;
        font-weight: bold;
    }

    &__subtitle {
        color: $text;
    }
}

</style>