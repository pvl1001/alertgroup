<template>
    <b-tabs no-nav-style pills card class="Tabs">
        <b-tab title="Информация" active>
            <b-card-text>
                <TabsSlider />
                <TabsPrice />

            </b-card-text>
        </b-tab>
        <b-tab title="Площади">
            <b-card-text></b-card-text>
        </b-tab>
        <b-tab title="Акции">
            <b-card-text></b-card-text>
        </b-tab>
        <b-tab title="Преимущества">
            <b-card-text></b-card-text>
        </b-tab>
    </b-tabs>
</template>

<script>

import TabsSlider from "@/components/Tabs_slider";
import TabsPrice from "@/components/Tabs_price";

export default {
    name: "Tabs",
    components: {
        TabsSlider,
        TabsPrice
    }
}
</script>

<style lang="scss">
@media (max-width: 767px) {
    .Tabs {
        margin-top: 1px;

        .tab-content {
            background-color: #E5E5E5;
            padding-bottom: 60px;
        }

        .card-header {
            overflow-x: auto;
            box-shadow: 0 4px 10px rgba(10, 61, 128, 0.05);
            background-color: #fff;
            border-bottom: 0;
        }

        .card-body {
            padding: 8px;
        }

        .nav {
            flex-wrap: nowrap;
        }

        .nav-pills .nav-link.active, .nav-pills .show > .nav-link {

        }

        .card-header {
            padding: 2px 8px;
            font-weight: bold;
            font-size: 14px;
            line-height: 24px;
            display: flex;
            align-items: center;

            a {
                color: #7C8A9D !important;
            }
        }

        .nav-link {
            padding: 8px 16px;
        }

        .nav-link.active {
            color: #343434 !important;
            position: relative;


            &:before {
                content: '';
                position: absolute;
                bottom: -2px;
                left: 0;
                background: #184F90;
                border-radius: 1px 1px 0 0;
                width: 100%;
                height: 2px;
            }
        }

        .Tabs-cont {
            background-color: #fff;
            box-shadow: 0 4px 10px rgba(10, 61, 128, 0.05);
            border-radius: 3px;
            padding: 16px;
            margin-bottom: 24px;
        }

    }
}

</style>