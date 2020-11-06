<template>
    <div class="Tabs-price">
        <div class="Tabs-cont collapse-wrapp">
            <div v-b-toggle.collapse-1 class="title">
                Стоимость
                <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M9 5L5 1L1 5" stroke="#184F90" stroke-width="2" stroke-linecap="round"
                          stroke-linejoin="round"/>
                </svg>

            </div>
            <b-collapse id="collapse-1" class="Tabs-price__collapse">
                <b-card>
                    <div class="Tabs-price__collapse_share">
                        С акцией месяца
                    </div>
                    <div class="Tabs-price__collapse_price">
                        <span>79 015 р./м²</span>
                        <span>3 870 900р.</span>
                    </div>
                    <div class="Tabs-price__collapse_title">
                        100% / ипотека
                    </div>
                    <div class="Tabs-price__collapse_price">
                        <span>79 015 р./м²</span>
                        <span>3 870 900р.</span>
                    </div>
                    <div class="Tabs-price__collapse_title">
                        Базовая
                    </div>
                    <div class="Tabs-price__collapse_price">
                        <span>79 015 р./м²</span>
                        <span>3 870 900р.</span>
                    </div>

                </b-card>
            </b-collapse>
        </div>

        <div class="Tabs-cont Tabs-price__raise">
            <span class="Tabs-price__raise_title">Прогнозируемое повышение на</span>
            <span class="Tabs-price__raise_price">120 321р.</span>
        </div>

        <div class="Tabs-cont Tabs-price__data">
            <div class="Tabs-price__data_card card-small">
                <div class="card-small__wrapp">
                    <span class="card-small__title">
                        Подъезд
                    </span>
                    <div class="card-small__number">17</div>
                </div>
            </div>
            <div class="Tabs-price__data_card card-small">
                <div class="card-small__wrapp">
                     <span class="card-small__title">
                        Этаж
                    </span>
                    <div class="card-small__number">17</div>
                </div>
            </div>
            <div class="Tabs-price__data_card card-small">
                <div class="card-small__wrapp">
                    <span class="card-small__title">
                        Комнат
                    </span>
                    <div class="card-small__number">17</div>
                </div>
            </div>
            <div class="Tabs-price__data_card card-small card-big">
                <div class="card-small__wrapp">
                    <span class="card-small__title">
                        Высота потолка
                    </span>
                    <div class="card-small__number">2.76м²</div>
                </div>
            </div>
            <div class="Tabs-price__data_card card-small card-big">
                <div class="card-small__wrapp">
                    <span class="card-small__title">
                        Вид из окна
                    </span>
                    <div class="card-small__number">Во двор и на улицу</div>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: "Tabs_price"
}
</script>

<style scoped lang="scss">

@media (max-width: 767px) {

    .Tabs-price {

        .title {
            font-weight: bold;
            font-size: 14px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            text-transform: uppercase;
            height: 49px;
            padding: 0 16px;
            margin-bottom: 0;

            svg {
                transition: .3s;
            }
        }

        .collapse-wrapp {
            margin-bottom: 10px;
            padding: 0;
        }

        .title.collapsed svg {
            transform: rotateX(180deg);
        }

        .card-body {
            padding: 0;
        }

        .card {
            border-radius: 0;
            border: 0;
        }

        .Tabs-price__collapse {
            border-top: 1px solid #EBEDF0;
            padding: 0 2px 2px;

            .Tabs-price__collapse_share {
                font-weight: 600;
                font-size: 14px;
                line-height: 170.23%;
                color: #7650A6;
                padding: 4px 14px;
            }

            .Tabs-price__collapse_price {
                display: flex;
                align-items: center;
                justify-content: space-between;
                background: #F6F7F8;
                border-radius: 2px;
                padding: 3px 14px 4px;

                span:first-child {
                    font-weight: 600;
                    font-size: 16px;
                    line-height: 170.23%;
                }

                span:last-child {
                    font-weight: bold;
                    font-size: 24px;
                    line-height: 41px;
                }
            }

            .Tabs-price__collapse_title {
                font-weight: 600;
                font-size: 14px;
                line-height: 170.23%;
                color: #4F5863;
                padding: 4px 14px;
            }
        }

        .Tabs-price__raise {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 9px 16px;
            margin-bottom: 24px;

            &_title {
                font-weight: bold;
                font-size: 12px;
                line-height: 170.23%;
                color: #2C323A;
            }

            &_price {
                font-weight: 600;
                font-size: 14px;
                line-height: 170.23%;
                color: #184F90;
            }
        }

        .Tabs-price__data {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin: -4px;
            background-color: transparent;
            padding: 0;

            .card-small {
                width: 33.33%;
                padding: 4px;
                text-align: center;
                font-size: 14px;

                &__wrapp {
                    background-color: #fff;
                    padding: 0 2px 2px 2px;
                    box-shadow: 0 4px 10px rgba(10, 61, 128, 0.05);
                    border-radius: 3px;
                }

                &__title {
                    color: #173456;
                    font-weight: bold;
                    line-height: 170.23%;
                    padding: 4px 0;
                    box-sizing: content-box;
                    display: block;
                }

                &__number {
                    background-color: #F6F7F8;
                    border-radius: 2px;
                    color: #2C323A;
                    font-weight: 600;
                    height: 40px;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                }
            }

            .card-big {
                width: 50%;
            }
        }
    }
}
</style>