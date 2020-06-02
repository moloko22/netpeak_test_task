<template>
    <section class="section_intro">
        <div  class="first_intro"><img src="../../assets/intro_icon.png" alt="intro"></div>
        <div  class="second_intro"><p><span>AppStarter. </span>Best landing page for web and mobile apps </p></div>
        <div class="third_intro">
            <button>Download Now</button>
            <button>Watch Video</button>
        </div>
    </section>
</template>
<style>
    .section_intro {
        position: absolute;
        width: 40%;
        height: 310px;
        left: 135px;
        top: 230px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-content: flex-start;
    }
    .second_intro {
        width: 555px;
        min-height: 100px;
        margin-bottom: 25px;
    }
    .second_intro p span {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 800;
        font-size: 35px;
        line-height: 50px;
        letter-spacing: 1px;
        color: #FFFFFF;
    }
    .second_intro p {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 35px;
        line-height: 50px;
        letter-spacing: 1px;
        color: #FFFFFF;
    }
    .third_intro {
        display: flex;
        width: 331px;
        justify-content: space-between;
    }
    .third_intro :first-child{
        width: 167px;
        min-height: 50px;
        border: none;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: bold;
        font-size: 17px;
        line-height: 23px;
        text-align: center;
        letter-spacing: 1px;
        color: #FFFFFF;
        background: linear-gradient(163.33deg, #FF8E64 0%, #FFE641 100%);
        border-radius: 6px;
    }
    .third_intro :last-child {
        width: 144px;
        min-height: 50px;
        border: none;
        background: #FFFFFF;
        border-radius: 6px;
        box-shadow: 0 6px 12px rgba(40, 43, 49, 0.08);
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: bold;
        font-size: 17px;
        line-height: 23px;
        text-align: center;
        letter-spacing: 1px;
        color: #282B31;
    }

</style>