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
            }
        },
        mounted() {
            document.querySelectorAll("ul[data-items]").forEach(function(element) {
                var ruler = element;
                ruler.innerHTML = '';
                var len = Number(ruler.getAttribute("data-items")) || 0;
                var item = document.createElement("li");
                for (var i = 1; i <= len; i++) {
                    var newItem = item.cloneNode();
                    newItem.textContent = (i * 0.5).toFixed(1);
                    ruler.appendChild(newItem);
                }
            });
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
                            <div class="skills__progress--bar" :style="{width: skill.progress }"></div>
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
</style>