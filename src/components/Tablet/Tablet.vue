<template>
    <section class="section_tablet">
        <div class="section_tablet_first_child">
            <div class="section_tablet_first_child_div">
                <img src="../../assets/tablet_photo.png" alt="tablet_photo">
            </div>
        </div>
    </section>
</template>
<style>
    .section_tablet{
        position: absolute;
        width: 30%;
        height: 708px;
        left: 785px;
        top: 140px;
    }
    .section_tablet_first_child{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 470px;
        min-height: 708px;
        position: absolute;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        border-radius: 60px;
        background: linear-gradient(180deg, rgba(255, 255, 255, 0.0001) 96.24%, rgba(32, 33, 39, 0.03) 100%), #FFFFFF;
        box-shadow: inset 0-2px 6px rgba(40, 43, 49, 0.06);
    }
    .section_tablet_first_child_div{
        position: absolute;
        left: 3.85%;
        right: 3.85%;
        top: 9.17%;
        bottom: 9.17%;
        width: 15%;
        min-height: 578px;
    }
    @media screen and (max-width: 1400px) and (min-width: 960px) {
        .section_tablet{
            position: absolute;
            width: 18%;
            height: 708px;
            left: 520px;
            top: 140px;
        }
    }
    @media screen and (max-width: 960px) and (min-width: 600px) {
        .section_tablet{
            position: absolute;
            width: 90%;
            height: 708px;
            left: 275px;
            top: 140px;
        }
        .section_tablet_first_child{
            display: flex;
            justify-content: center;
            align-items: center;
            width: 65%;
            min-height: 600px;
            position: absolute;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            border-radius: 60px;
            background: linear-gradient(180deg, rgba(255, 255, 255, 0.0001) 96.24%, rgba(32, 33, 39, 0.03) 100%), #FFFFFF;
            box-shadow: inset 0-2px 6px rgba(40, 43, 49, 0.06);
        }
        .section_tablet_first_child_div{
            position: absolute;
            left: 2%;
            right: 3.85%;
            top: 9.17%;
            bottom: 9.17%;
            width: 100%;
            min-height: 578px;
        }
        .section_tablet_first_child_div img {
            width: 400px;
        }
    }
    @media screen and(max-width: 600px) and (min-width: 300px){
        .section_tablet{
            position: absolute;
            width: 600px;
            height: 708px;
            left: 275px;
            top: 140px;
        }
        .section_tablet_first_child{
            display: flex;
            justify-content: center;
            align-items: center;
            width: 65%;
            min-height: 600px;
            position: absolute;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            border-radius: 60px;
            background: linear-gradient(180deg, rgba(255, 255, 255, 0.0001) 96.24%, rgba(32, 33, 39, 0.03) 100%), #FFFFFF;
            box-shadow: inset 0-2px 6px rgba(40, 43, 49, 0.06);
        }
        .section_tablet_first_child_div{
            position: absolute;
            right: 3.85%;
            left: 0;
            top: 9.17%;
            bottom: 9.17%;
            width: 100%;
            min-height: 578px;
        }
        .section_tablet_first_child_div img {
            position: absolute;
            left: 25px;
            width: 400px;
        }
    }
</style>