<script>
    import socialMedia from './socialMedia.vue';
    export default {
        components: {
            socialMedia
        }
    }
</script>

<template>
    <footer class="footer">
        <span>Copyright © Gabriel Henrique Selani Barbosa - 2024</span>
    </footer>
</template>

<style lang="scss">
    .footer {
        width: calc(100% + 44px);
        height: 42px;
        background: #131414;
        margin: 30px 0 0 -22px;
        padding: 15px 20px;
        span {
            color: rgba(255, 255, 255, 0.50);
            text-align: center;
            font-size: 11px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
            display: block;
        }
    }
</style>