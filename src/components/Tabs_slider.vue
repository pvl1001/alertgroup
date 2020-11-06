<template>
    <div class="Tabs-cont Tabs-slider">
        <div class="slide-border">
            <VueSlickCarousel class="slider-home" v-bind="settings">
                <div class="slider-img">
                    <img src="../assets/img/image 5.png"/>
                </div>
                <div class="slider-img">
                    <img src="https://static.wixstatic.com/media/34ba65_fe4a01661ba54a50be1da8e192ca09ed.jpg"/>
                </div>
                <div class="slider-img">
                    <img src="https://rbi.ru/upload/kelnik.estate/d32/91b1236c79e2c0bbcd60da2133e26e5c.jpg"/>
                </div>
                <div class="slider-img">
                    <img src="https://astropro.ru/img/srmn33ogoqc/9wzsc2bte.jpg"/>
                </div>
                <div class="slider-img">
                    <img src="https://d1-dom.ru/upload/iblock/fc7/fc703d4139e49fc63f8bebf9e6c1b740.png"/>
                </div>
            </VueSlickCarousel>
        </div>
    </div>
</template>

<script>
export default {
    name: "Tabs_slider",

    data() {
        return {
            settings: {
                slidesToShow: 1,
                slidesToScroll: 1,
                dots: true,
                arrows: false
            }
        }
    }
}
</script>

<style lang="scss">

@media (max-width: 767px) {

    .Tabs-slider {
        .slide-border {
            border: 1px solid #E2E5E9;
            border-radius: 3px;
        }

        .tab-content {
            background-color: #E5E5E5;
        }

        .slider-img {
            height: 327px;
            border-radius: 3px;
            padding: 18px;
            font-size: 0;
            white-space: nowrap;
            text-align: center;

            &:before {
                content: '';
                display: inline-block;
                vertical-align: middle;
                height: 100%;
            }

            img {
                display: inline-block !important;
                vertical-align: middle;
            }
        }

        .slick-dots {
            bottom: -13px;
            height: 16px;

            li {
                margin: 0;
                width: 9px;

                button:before {
                    font-size: 5px;
                }
            }

            li.slick-active button:before {
                color: #184F90;
                opacity: 1;
            }
        }
    }

}

</style>