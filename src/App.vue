<template>
    <div id="app">
        <div class="card">
            <div class="card__name">
                <h1>Карточка квартиры</h1>
                <button class="card__close"></button>
            </div>
            <div class="card__description">
                <div class="card__description_number">№12</div>
                <div class="card__description_metr">
                    <span>M</span>
                    <span>59.52м²</span>
                </div>
                <div class="card__description_free">Свободно</div>
            </div>
            <Tabs />
            <Nav />
        </div>
    </div>
</template>

<script>
import Tabs from "@/components/Tabs";
import Nav from "@/components/Nav";

export default {
    name: 'App',
    components: {
        Tabs,
        Nav
    },

}
</script>

<style lang="scss">
@import '~bootstrap';
@import '~bootstrap-vue';

* {
    padding: 0;
    margin: 0;
    border: 0;
}


*,
*:before,
*:after {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}

img {
    max-width: 100%;
    max-height: 100%;
}

:focus,
:active {
    outline: none;
}

a:focus,
a:active {
    outline: none;
}


nav,
footer,
header,
aside {
    display: block;
}


html,
body {
    height: 100%;
    width: 100%;
    line-height: 1;
    font-size: 14px;
    -ms-text-size-adjust: 100%;
    -moz-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
}


input,
button,
textarea {
    font-family: inherit;
}


input::-ms-clear {
    display: none;
}

button {
    cursor: pointer;
}

button::-moz-focus-inner {
    padding: 0;
    border: 0;
}

a,
a:visited {
    text-decoration: none;
}

a:hover {
    text-decoration: none;
}

ul li {
    list-style: none;
}

img {
    vertical-align: top;
}

h1,
h2,
h3,
h4,
h5,
h6 {
    font-size: inherit;
    font-weight: 400;
}

//Сброс cтилей


@media (max-width: 767px) {

    body, html {
        font-family: "Open Sans", sans-serif;
        color: #2C323A;
    }

    h1 {

    }

    .card__name {
        min-height: 60px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        box-shadow: 0 4px 10px rgba(10, 61, 128, 0.05);

        h1 {
            font-weight: bold;
            font-size: 18px;
            line-height: 25px;
            text-transform: uppercase;
            padding-left: 16px;
        }
    }

    .card__close {
        width: 60px;
        height: 60px;
        background: url('./assets/svg/close.svg') center / 9px no-repeat;
        position: relative;

        &:before {
            content: '';
            display: block;
            height: 36px;
            width: 1px;
            background-color: #E2E5E9;
            position: absolute;
            left: 0;
            top: calc(50% - 18px);
        }
    }

    .card__description {
        display: flex;
        padding: 9px 12px 8px 8px;
        font-size: 14px;
        box-shadow: 0 4px 10px rgba(10, 61, 128, 0.05);
        font-weight: bold;

        &_number {
            margin-right: 4px;
            padding: 4px 8px;
            border: 1px solid #E2E5E9;
            border-radius: 3px;
        }

        &_metr {
            border: 1px solid #E2E5E9;
            border-radius: 3px;

            span{
                display: inline-block;
                height: 100%;
                line-height: 22px;
            }

            span:first-child {
                padding: 0 7px 0 9px;
                border-right:  1px solid #E2E5E9;
            }
            span:last-child {
                padding: 0 8px 0 9px;
            }
        }

        &_free {
            margin-left: auto;
            font-weight: 600;
            font-size: 12px;
            line-height: 20px;
            display: flex;
            align-items: center;
            text-align: center;
            color: #FFFFFF;
            background: #44A86E;
            border-radius: 32px;
            padding: 1px 10px 2px;
        }
    }
}

</style>
