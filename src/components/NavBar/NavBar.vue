<template>
    <section class="section_navbar">
        <div>
            <h3>AppStarter</h3>
        </div>
        <div>
            <nav>
                <ul>
                    <li><a href="#">Features</a></li>
                    <li><a href="#">Video Tour</a></li>
                    <li><a href="#">Reviews</a></li>
                    <li><a href="#">Pricing</a></li>
                </ul>
            </nav>
            <button class="button">GET IT FREE</button>
        </div>
    </section>
</template>
<style>
    .section_navbar{
        width: 50%;
        display: flex;
        justify-content: space-around;
    }
    .section_navbar div {
        display: flex;
        align-content: center;
    }
    .section_navbar div h3 {
        position: absolute;
        width: 20%;
        height: 27px;
        left: 135px;
        top: 30px;
        font-family: Nunito Sans,serif;
        font-style: normal;
        font-weight: 800;
        font-size: 20px;
        line-height: 27px;
        color: #FFFFFF;
    }
    .section_navbar nav {
        position: absolute;
        width: 25%;
        height: 20px;
        left: 815px;
        top: 35px;
    }
    .section_navbar button {
        position: absolute;
        width: 10%;
        height: 40px;
        left: 1170px;
        top: 25px;
        background: #FFFFFF;
        border: none;
        border-radius: 6px;
    }
    .button {
        font-family: Nunito Sans,serif;
        font-style: normal;
        font-weight: bold;
        font-size: 14px;
        line-height: 19px;
        text-align: center;
        letter-spacing: 1px;
        color: #282B31;
    }
    .section_navbar ul{
        display: flex;
        justify-content: space-around;
    }
    .section_navbar li {
        list-style: none;
    }
    .section_navbar li a {
        text-decoration: none;
        font-family: Nunito Sans,serif;
        font-style: normal;
        font-weight: normal;
        font-size: 15px;
        line-height: 20px;
        color: #FFFFFF;
    }
    @media screen and (max-width: 1400px) and (min-width: 960px) {
        .section_navbar nav {
            position: absolute;
            width: 25%;
            height: 20px;
            left: 550px;
            top: 35px;
        }
        .section_navbar button {
            position: absolute;
            width: 10%;
            height: 40px;
            left: 85%;
            top: 25px;
            background: #FFFFFF;
            border: none;
            border-radius: 6px;
        }
    }
    @media screen and (max-width: 960px) and (min-width: 600px) {
        .section_navbar nav {
            position: absolute;
            width: 40%;
            height: 20px;
            left: 280px;
            top: 35px;
        }
        .section_navbar button {
            position: absolute;
            width: 10%;
            height: 40px;
            left: 600px;
            top: 25px;
            background: #FFFFFF;
            border: none;
            border-radius: 6px;
        }
    }
    @media screen and (max-width: 600px) and (min-width: 300px) {
        .section_navbar nav {
            position: absolute;
            width: 60%;
            height: 20px;
            left: 120px;
            top: 35px;
        }
        .section_navbar div h3 {
            position: absolute;
            width: 20%;
            height: 27px;
            left: 8px;
            top: 30px;
            font-family: Nunito Sans,serif;
            font-style: normal;
            font-weight: 800;
            font-size: 20px;
            line-height: 27px;
            color: #FFFFFF;
        }
        .section_navbar button {
            position: absolute;
            width: 10%;
            height: 40px;
            left: 400px;
            top: 25px;
            background: #FFFFFF;
            border: none;
            border-radius: 6px;
        }
        .button {
            font-family: Nunito Sans,serif;
            font-style: normal;
            font-weight: bold;
            font-size: 12px;
            line-height: 19px;
            text-align: center;
            letter-spacing: 1px;
            color: #282B31;
        }
    }
</style>
