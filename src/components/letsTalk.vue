<script>
    export default {
        data() {
            return {
                email: 'gabrielbarbosa61@gmail.com'
            }
        },
        methods: {
            copy() {
                navigator.clipboard.writeText(this.email);
            }
        }
    }
</script>

<template>
    <section>
        <div class="lets-talk">
            <h4>letsTalk<b>()</b></h4>
            <ul class="lets-talk__list">
                <li class="lets-talk__wpp">
                    <a href="" target="_blank">
                        <i></i> Vamos Conversar
                    </a>
                </li>
                <li class="lets-talk__email">
                    <i></i>
                    <span>E-mail:</span>
                    <input :value="email" readonly="readonly">
                    <button @click="copy()"><i></i></button>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss">
    .lets-talk {
        margin-top: 100px;
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
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 20px;
        }
        &__wpp {
            width: 200px;
            height: 40px;
            border-radius: 16px;
            border: 1px solid #41B883;
            margin: 20px 10px 0;
            a {
                height: 100%;
                color: #41B883;
                font-size: 12px;
                font-style: normal;
                font-weight: 600;
                line-height: normal;
                text-decoration: initial;
                display: flex;
                justify-content: center;
                align-items: center;
                i {
                    background: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzgiIGhlaWdodD0iMzgiIHZpZXdCb3g9IjAgMCAzOCAzOCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTYuNzM5MSAyNi4yNzI3QzQuOTcxMDQgMjMuMjg5NyA0LjM1MjU5IDE5Ljc2MzkgNC45OTk4NiAxNi4zNTczQzUuNjQ3MTQgMTIuOTUwNiA3LjUxNTYxIDkuODk3MzkgMTAuMjU0NSA3Ljc3MDc0QzEyLjk5MzQgNS42NDQwOSAxNi40MTQ0IDQuNTkwMyAxOS44NzUyIDQuODA3MTlDMjMuMzM2IDUuMDI0MDcgMjYuNTk4NiA2LjQ5NjczIDI5LjA1MDYgOC45NDg2OUMzMS41MDI2IDExLjQwMDcgMzIuOTc1MiAxNC42NjMzIDMzLjE5MjEgMTguMTI0MUMzMy40MDkgMjEuNTg0OSAzMi4zNTUyIDI1LjAwNTkgMzAuMjI4NSAyNy43NDQ4QzI4LjEwMTkgMzAuNDgzNyAyNS4wNDg3IDMyLjM1MjIgMjEuNjQyIDMyLjk5OTRDMTguMjM1NCAzMy42NDY3IDE0LjcwOTYgMzMuMDI4MyAxMS43MjY2IDMxLjI2MDJWMzEuMjYwMkw2Ljc5ODQ3IDMyLjY1NTVDNi41OTY1NiAzMi43MTQ2IDYuMzgyNDkgMzIuNzE4MiA2LjE3ODY4IDMyLjY2NjFDNS45NzQ4OCAzMi42MTM5IDUuNzg4ODUgMzIuNTA3OSA1LjY0MDEgMzIuMzU5MkM1LjQ5MTM0IDMyLjIxMDQgNS4zODUzNSAzMi4wMjQ0IDUuMzMzMjEgMzEuODIwNkM1LjI4MTA4IDMxLjYxNjggNS4yODQ3MyAzMS40MDI3IDUuMzQzNzggMzEuMjAwOEw2LjczOTEgMjYuMjcyN1oiIHN0cm9rZT0iIzQxQjg4MyIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0yMi41Nzc0IDI3LjMxMTZDMjEuMDE0OSAyNy4zMTU1IDE5LjQ2NyAyNy4wMTA2IDE4LjAyMjcgMjYuNDE0NUMxNi41Nzg0IDI1LjgxODMgMTUuMjY2MSAyNC45NDI3IDE0LjE2MTMgMjMuODM3OEMxMy4wNTY0IDIyLjczMyAxMi4xODA4IDIxLjQyMDcgMTEuNTg0NiAxOS45NzY0QzEwLjk4ODUgMTguNTMyMSAxMC42ODM2IDE2Ljk4NDIgMTAuNjg3NSAxNS40MjE3QzEwLjY5MTUgMTQuMzIyIDExLjEzMTEgMTMuMjY4NiAxMS45MTAxIDEyLjQ5MjRDMTIuNjg5MSAxMS43MTYyIDEzLjc0NCAxMS4yODAzIDE0Ljg0MzggMTEuMjgwM1YxMS4yODAzQzE1LjAyNTIgMTEuMjc4OSAxNS4yMDM3IDExLjMyNjMgMTUuMzYwNCAxMS40MTc4QzE1LjUxNzIgMTEuNTA5MiAxNS42NDY0IDExLjY0MTIgMTUuNzM0NCAxMS43OTk4TDE3LjQ3MTEgMTQuODI4QzE3LjU3NDQgMTUuMDEyIDE3LjYyNzQgMTUuMjIwMSAxNy42MjQ4IDE1LjQzMTFDMTcuNjIyMiAxNS42NDIyIDE3LjU2NDEgMTUuODQ4OCAxNy40NTYzIDE2LjAzMDNMMTYuMDYxIDE4LjM2MDhDMTYuNzc1NyAxOS45NTA3IDE4LjA0ODQgMjEuMjIzNCAxOS42MzgzIDIxLjkzODFMMjEuOTY4OCAyMC41NDI4QzIyLjE1MDMgMjAuNDM1IDIyLjM1NjkgMjAuMzc2OSAyMi41NjggMjAuMzc0M0MyMi43NzkgMjAuMzcxNyAyMi45ODcxIDIwLjQyNDcgMjMuMTcxMSAyMC41MjhMMjYuMTk5MyAyMi4yNjQ3QzI2LjM1NzkgMjIuMzUyNyAyNi40ODk5IDIyLjQ4MTkgMjYuNTgxMyAyMi42Mzg3QzI2LjY3MjcgMjIuNzk1NCAyNi43MjAyIDIyLjk3MzkgMjYuNzE4OCAyMy4xNTUzQzI2LjcxNDkgMjQuMjUzOSAyNi4yNzc4IDI1LjMwNjUgMjUuNTAyNCAyNi4wODQ3QzI0LjcyNyAyNi44NjI5IDIzLjY3NTkgMjcuMzAzNyAyMi41Nzc0IDI3LjMxMTZWMjcuMzExNloiIHN0cm9rZT0iIzQxQjg4MyIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+Cjwvc3ZnPgo=)no-repeat;
                    background-size: 100%;
                    width: 30px;
                    height: 30px;
                    display: inline-block;
                    margin-right: 5px;
                }
            }
        }
        &__email {
            margin: 20px 10px 0;
            width: 200px;
            display: grid;
            grid-template-columns: 1fr;
            grid-template-rows: 20px 20px 27px 27px;
            i {
                background: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHZpZXdCb3g9IjAgMCA0MCA0MCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTMyLjg1OTQgNS42MDgyM0wzLjczNDM3IDEzLjgxMTRDMy40ODY0NCAxMy44NzkxIDMuMjY1NDQgMTQuMDIxNyAzLjEwMTQ2IDE0LjIxOTZDMi45Mzc0OCAxNC40MTc1IDIuODM4NSAxNC42NjEyIDIuODE4MDEgMTQuOTE3NEMyLjc5NzUxIDE1LjE3MzYgMi44NTY0OSAxNS40Mjk5IDIuOTg2OTIgMTUuNjUxNEMzLjExNzM0IDE1Ljg3MjkgMy4zMTI4NyAxNi4wNDg4IDMuNTQ2ODcgMTYuMTU1MUwxNi45MjE5IDIyLjQ4MzJDMTcuMTgzOSAyMi42MDQ2IDE3LjM5NDMgMjIuODE1IDE3LjUxNTYgMjMuMDc3TDIzLjg0MzcgMzYuNDUyQzIzLjk1MDEgMzYuNjg2IDI0LjEyNiAzNi44ODE1IDI0LjM0NzQgMzcuMDExOUMyNC41Njg5IDM3LjE0MjQgMjQuODI1MiAzNy4yMDEzIDI1LjA4MTQgMzcuMTgwOEMyNS4zMzc2IDM3LjE2MDMgMjUuNTgxMyAzNy4wNjE0IDI1Ljc3OTIgMzYuODk3NEMyNS45NzcxIDM2LjczMzQgMjYuMTE5NyAzNi41MTI0IDI2LjE4NzUgMzYuMjY0NUwzNC4zOTA2IDcuMTM5NDhDMzQuNDUyOCA2LjkyNjk0IDM0LjQ1NjYgNi43MDE2IDM0LjQwMTcgNi40ODcwN0MzNC4zNDY5IDYuMjcyNTMgMzQuMjM1MyA2LjA3NjcxIDM0LjA3ODcgNS45MjAxM0MzMy45MjIxIDUuNzYzNTUgMzMuNzI2MyA1LjY1MTk4IDMzLjUxMTggNS41OTcxQzMzLjI5NzMgNS41NDIyMiAzMy4wNzE5IDUuNTQ2MDcgMzIuODU5NCA1LjYwODIzVjUuNjA4MjNaIiBzdHJva2U9IiM0MUI4ODMiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cGF0aCBkPSJNMTcuMzI4MSAyMi42NzA5TDI0LjM5MDYgMTUuNjA4NCIgc3Ryb2tlPSIjNDFCODgzIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==)no-repeat;
                background-size: 100%;
                width: 20px;
                height: 20px;
                display: block;
                margin: 0 auto;
            }
            span {
                color: #41B883;
                text-align: center;
                font-size: 14px;
                font-style: normal;
                font-weight: 400;
                line-height: normal;
            }
            input {
                border: none;
                width: 100%;
                background: transparent;
                color: rgba(255, 255, 255, 0.50);
                text-align: center;
                font-size: 14px;
                font-style: normal;
                font-weight: 400;
                line-height: normal
            }
            button {
                appearance: none;
                background: transparent;
                border: none;
                cursor: pointer;
                width: 25px;
                margin: 0 auto;
                margin-top: 10px;
                i {
                    background: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzIiIGhlaWdodD0iMzIiIHZpZXdCb3g9IjAgMCAzMiAzMiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTI3IDIyLjk5OVY0Ljk5OTAySDkiIHN0cm9rZT0iIzQxQjg4MyIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0yMyA4Ljk5OTAySDVWMjYuOTk5SDIzVjguOTk5MDJaIiBzdHJva2U9IiM0MUI4ODMiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K)no-repeat;
                    background-size: 100%;
                    width: 25px;
                    height: 25px;
                    display: block;
                }
            }
        }
    }
    
</style>