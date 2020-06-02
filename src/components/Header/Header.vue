<template>
    <header>
        <div class="header_background"></div>
        <NavBar></NavBar>
        <Intro></Intro>
        <Tablet></Tablet>
    </header>
</template>
<script>
    import NavBar from '../NavBar/NavBar';
    import Intro from '../Intro/Intro';
    import Tablet from '../Tablet/Tablet';
    export default {
        components: {
            NavBar,
            Intro,
            Tablet
        }
    }
</script>
<style>
    header {
        position: relative;
        width: 100%;
        min-height: 900px;
        color: #FFFFFF;
        background: #F8F9FA;
    }
    .header_background {
        width: 100%;
        position: absolute;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        min-height: 900px;
        background-image: url('../../assets/header_background.png');
        background-repeat: no-repeat;
    }
</style>
