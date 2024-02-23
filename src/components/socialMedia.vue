<script>
    import linkedinIcon from './icons/linkedinIcon.vue';
    import githubIcon from './icons/githubIcon.vue';

    export default {
        components: {
            linkedinIcon,
            githubIcon
        }
    }
</script>

<template>
    <section>
        <ul class="social-media">
            <li class="social-media__item">
                <a href="https://www.linkedin.com/in/gabriel-henrique-selani-barbosa-8323b7151/" target="_blank" class="social-media__link">
                    <linkedinIcon />
                </a>
            </li>
            <li class="social-media__item">
                <a href="https://github.com/Gabriel-Henrique-Selani-Barbosa" target="_blank" class="social-media__link">
                    <githubIcon />
                </a>
            </li>
        </ul>
    </section>
</template>

<style lang="scss">
    .social-media {
        display: flex;
        justify-content: center;
        &__item {
            margin: 0 8px;
            width: 32px;
            height: 32px;
        }
    }
</style>