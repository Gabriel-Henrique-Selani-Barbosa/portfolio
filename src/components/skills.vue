<script>
    import skillsIcon from '@/components/icons/skillsIcon.vue';
    import jsonSktacks from '@/json/stacks.json';

    export default {
        components: {
            skillsIcon
        },
        data() {
            return {
                skills: jsonSktacks,
                sizes: 10,
                screen,
            }
        },
        mounted() {
            this.screen = window.outerWidth;
        }
    }
</script>

<template>
    <section>
        <div class="skills">
            <h4>skills<b>()</b></h4>
                <ul class="skills__list">
                    <li class="skills__item" 
                        v-for="(skill, index) in skills"
                        :key="skill.name"
                        :index="index"
                        :class="{'last': index == skills.length - 1}"
                    >
                        <div class="skills__square">
                            <skillsIcon :icon-name="skill.id"/>
                            <span class="skills__name" v-text="skill.name"></span>
                        </div>
                        <div class="skills__progress">
                            <div class="skills__progress--bar" :style="[screen <= 767 ? {width: skill.progress} : {height: skill.progress}]"></div>
                        </div>
                    </li>
                </ul>
                <ul class="skills__ruler">
                    <li v-for="index in 10" v-text="(index * 0.5).toFixed(1)"></li>
                </ul>
        </div>
    </section>
</template>

<style lang="scss">
    .skills {
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
            margin-top: 40px;
        }
        @media screen and (max-width: 767px) {
            &__item {
                display: flex;
                align-items: center;
                &.last {
                    .skills__square {
                        position: relative;
                        &::before {
                            content: "";
                            background: rgba(255, 255, 255, 0.5);
                            width: 1px;
                            height: 20px;
                            display: block;
                            position: absolute;
                            top: 100%;
                            right: -1px;
                        }
                    }
                }
            }
            &__square {
                width: 80px;
                height: 96px;
                padding-right: 20px;
                border-right: 1px solid rgba(255, 255, 255, 0.5);
                svg {
                    width: 100%;
                    height: calc(100% - 34px);
                }
            }
            &__name {
                color: #41B883;
                text-align: center;
                font-size: 12px;
                font-style: normal;
                font-weight: 400;
                line-height: normal;
                display: block;
                padding: 5px 0 15px;
            }
            &__progress {
                height: 24px;
                width: calc(100% - 80px);
                &--bar {
                    background: linear-gradient(90deg, #34495E 18.63%, #41B883 78.88%);
                    height: 24px;
                }
            }
            &__ruler {
                width: calc(100% - 60px);
                display: flex;
                border-top: 1px solid rgba(255, 255, 255, 0.5);
                justify-content: space-between;
                margin-left: auto;
                position: relative;
                padding-left: 20px;
                padding-top: 5px;
                li {
                    color: #fff;
                    font-size: 9px;
                    transform: translateX(50%);
                    position: relative;
                    &::before {
                        content: "";
                        width: 1px;
                        height: 7px;
                        background: rgba(255, 255, 255, 0.5);
                        position: absolute;
                        left: 50%;
                        transform: translateX(-50%);
                        top: -13px;
                    }
                }
            }
        }
        @media screen and (min-width: 768px) {
            position: relative;
            &__list {
                display: flex;
                flex-wrap: wrap;
                width: 650px;
                margin-left: 40px;
                position: relative;
                &::before {
                    content: "";
                    background: rgba(255, 255, 255, 0.5);
                    width: 20px;
                    height: 1px;
                    position: absolute;
                    bottom: 0;
                    left: -20px;
                }
            }
            &__item {
                width: 65px;
                height: 400px;
                border-bottom: 1px solid rgba(255, 255, 255, 0.5);
            }
            &__square {
                width: 65px;
                height: 120px;
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                svg {
                    width: 50px;
                    height: 50px;
                }
            }
            &__name {
                color: #41B883;
                text-align: center;
                font-size: 12px;
                font-style: normal;
                font-weight: 400;
                line-height: normal;
                display: block;
                padding: 5px 0 15px;
            }
            &__progress {
                height: calc(100% - 120px);
                width: 24px;
                position: relative;
                left: 50%;
                transform: translateX(-50%);
                display: flex;
                align-items: end;
                &--bar {
                    background: linear-gradient(0deg, #34495E 18.63%, #41B883 78.88%);
                    width: 24px;
                }
            }
            &__ruler {
                display: flex;
                flex-direction: column-reverse;
                border-right: 1px solid rgba(255, 255, 255, 0.5);
                height: 284px;
                position: absolute;
                bottom: -5px;
                left: 5px;
                justify-content: space-between;
                padding-right: 10px;
                padding-bottom: 20px;
                li {
                    color: #fff;
                    font-size: 9px;
                    transform: translateY(-50%);
                    position: relative;
                    &::before {
                        content: "";
                        width: 7px;
                        height: 1px;
                        background: rgba(255, 255, 255, 0.5);
                        position: absolute;
                        top: 50%;
                        transform: translateY(-50%);
                        left: 23px;
                    }
                }
            }
        }
    }
</style>