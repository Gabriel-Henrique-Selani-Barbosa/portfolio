<script>
    import languagesList from '@/json/languages.json';

    export default {
        data() {
            return {
                languages: languagesList
            }
        }
    }
</script>

<template>
    <section>
        <div class="language">
            <h4>Language<b>()</b></h4>
            <ul class="language__list">
                <li class="language__item" v-for="item in languages">
                    <span class="language__name" v-text="item.name"></span>
                    <div class="language__progress" :style="{ width: item.progress }" :data-progress="item.level"></div>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss">
    .language {
        margin-top: 80px;
        h4 {
            font-size: 30px;
            font-style: normal;
            font-weight: 700;
            line-height: normal;
            color: rgba(255, 255, 255, 0.5);
            b {
                color: #fff;
                font-family: "Roboto Mono", monospace;
            }
        }
        &__list {
            margin-top: 20px;
        }
        &__item {
            display: grid;
            grid-template-columns: 1fr;
            grid-template-rows: repeat(2, 1fr);
            margin-bottom: 20px;
        }
        &__name {
            grid-area: 1/1/2/2;
            color: #fff;
            font-size: 12px;
            font-style: normal;
            font-weight: 600;
            line-height: normal;
            letter-spacing: 1.477px;
        }
        &__progress {
            grid-area: 2/1/3/2;
            height: 12px;
            border-radius: 50px;
            background: linear-gradient(90deg, #34495E 18.63%, #41B883 78.88%);
            margin-top: 5px;
            position: relative;
            &::before {
                content: attr(data-progress);
                color: #fff;
                font-size: 10px;
                font-weight: 600;
                position: absolute;
                right: 0;
                top: 15px;
            }
        }
    }
</style>