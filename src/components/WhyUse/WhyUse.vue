<template>
    <section class="why_use">
        <div class="app_timer_info">
            <h3><span>Why</span> do we use it?</h3>
            <p>This sounded nonsense to Alice, so she said nothing, but set off at once toward the Red Queen.
                To her surprise, she lost sight of her in a moment.
            </p>
        </div>
        <AppTimer></AppTimer>
    </section>
</template>
<script>
    import AppTimer from "@/components/AppTimer/AppTimer";
    export default {
        components: {
            AppTimer,
        },
    }
</script>
<style>
    .why_use {
        width: 100%;
        min-height: 700px;
        background-image: url('../../assets/header_background.png');
        background-repeat: no-repeat;
    }
    .app_timer_info{
        position: absolute;
        width: 25%px;
        height: 50px;
        left: 435px;
        top: 1711px;
        min-height: 120px;
        display: flex;
        flex-direction: column;
    }
    .app_timer_info h3 span {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 800;
        font-size: 35px;
        line-height: 50px;
        text-align: center;
        letter-spacing: 1px;
        color: #FFFFFF;
    }
    .app_timer_info h3 {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 35px;
        line-height: 50px;
        text-align: center;
        letter-spacing: 1px;
        color: #FFFFFF;
    }
    .app_timer_info p {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 30px;
        text-align: center;
        color: rgba(255, 255, 255, 0.8);
    }
</style>