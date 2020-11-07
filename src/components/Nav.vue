<template>
    <div class="Nav">
        <img src="../assets/img/Subtract.png"  />
        <button class="Nav__btn btn-other"></button>
        <button class="Nav__btn btn-like"></button>
        <button class="Nav__btn btn-params"></button>
        <button class="Nav__btn btn-add"></button>
        <button class="btn-send"></button>
    </div>
</template>

<script>
export default {
    name: "Nav"
}
</script>

<style scoped lang="scss">

@media (max-width: 767px) {

    .Nav {
        position: fixed;
        z-index: 10;
        left: 0;
        bottom: 0;
        height: 60px;
        width: 100%;
        display: flex;
        align-items: center;
        border-radius: 10px 10px 0 0;
        overflow: hidden;

        &:before {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            background-color: #fff;
            border-radius: 15px 0 0 15px;
            height: 60px;
            width: 60%;
            z-index: 11;
        }

        img {
            position: absolute;
            bottom: -9px;
            right: -9px;
            height: 81px;
            max-height: none;
            max-width: none;
        }

        .Nav__btn {
            width: 19%;
            height: 44px;
            position: relative;
            z-index: 12;

            &:before {
                content: '';
                position: absolute;
                right: 0;
                top: calc(50% - 8px);
                width: 1px;
                height: 16px;
                background: #F0F2F4;
                border-radius: 4px;
            }
        }

        .Nav__btn.btn-add:before {
            display: none;
        }

        .btn-other {
            background: url('../assets/svg/other.svg') center no-repeat;
        }

        .btn-like {
            background: url('../assets/svg/like.svg') center no-repeat;
        }

        .btn-params {
            background: url('../assets/svg/params.svg') center no-repeat;
        }

        .btn-add {
            background: url('../assets/svg/add.svg') center no-repeat;
        }

        .btn-send {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: #fff url('../assets/svg/send.svg') center / 20px no-repeat;
            box-shadow: 0 2px 10px rgba(10, 61, 128, 0.1);
            position: fixed;
            right: 26px;
            bottom: 33px;
        }
    }

}

</style>