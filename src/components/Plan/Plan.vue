<template>
    <section class="section_plan">
        <div class="choose_plan">
            <div class="choose_plan_header">
                <h3><span>Choose</span> your plan</h3>
            </div>
            <div class="choose_plan_info">
                <p>This sounded nonsense to Alice, so she said nothing, but set off at once toward the Red Queen. To her surprise, she lost sight of her in a moment, and found herself walking.</p>
            </div>
            <div class="choose_plan_licenses">
                <p>
                Select the number of licenses:
                </p>
                <label for="plan">
                    <select name="plan" id="plan">
                        <option value="1">1</option>
                    </select>
                </label>
            </div>
            <div class="choose_plan_promo">
                <p>Enter the promo code:</p>
            </div>
            <div class="choose_plan_apply">
                <label>
                    <input type="text" placeholder="Promo code" class="choose_plan_apply_input">
                </label>
                    <button class="choose_plan_apply_button">Apply</button>
            </div>
        </div>
        <div class="plan_professional">
            <div>
                <p>Professional</p>
            </div>
            <div>
                <p>10$</p>
            </div>
            <div>
                <ul>
                    <li><img src="../../assets/check_icon_white.png" alt="ok_icon">Hundreds of elements</li>
                    <li><img src="../../assets/check_icon_white.png" alt="ok_icon">Style guide</li>
                    <li><img src="../../assets/check_icon_white.png" alt="ok_icon">160 icons included</li>
                    <li><img src="../../assets/check_icon_white.png" alt="ok_icon">Sketch files</li>
                    <li><img src="../../assets/check_icon_white.png" alt="ok_icon">Commercial license</li>
                </ul>
            </div>
            <div>
                <button class="plan_buttons">Buy Now</button>
            </div>
        </div>
        <div class="plan_starter">
            <div>
                <p>Starter</p>
            </div>
            <div>
                <p>Free</p>
            </div>
            <div>
                <ul>
                    <li><img src="../../assets/check_icon_black.png" alt="ok_icon">Hundreds of elements</li>
                    <li><img src="../../assets/check_icon_black.png" alt="ok_icon">Style guide</li>
                    <li><img src="../../assets/check_icon_black.png" alt="ok_icon">30 icons included</li>
                    <li><img src="../../assets/check_icon_black.png" alt="ok_icon">Personal license</li>
                </ul>
            </div>
            <div>
                <button class="plan_buttons">Get Free</button>
            </div>
        </div>
    </section>
</template>
<script>
    export default {
        components: {

        }
    }
</script>
<style>
    .section_plan {
        background: #F8F9FA;
        width: 100%;
        min-height: 750px;
        display: flex;
    }
    .section_plan p {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 30px;
        color: #676C75;
    }
    .choose_plan {
        position: absolute;
        width: 370px;
        height: 331px;
        left: 135px;
        top: 1058px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .choose_plan_header h3 span{
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 800;
        font-size: 35px;
        line-height: 50px;
        letter-spacing: 1px;
        color: #282B31;
    }
    .choose_plan_header h3 {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 35px;
        line-height: 50px;
        letter-spacing: 1px;
        color: #282B31;
    }
    .choose_plan_info {
        width: 370px;
        min-height: 120px;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 30px;
        color: #676C75;
    }

    .choose_plan_licenses {
        display: flex;
        justify-content: space-between;
        width: 305px;
        align-items: center;
        align-content: center;
    }
    .choose_plan_licenses select {
        width: 89px;
        border: none;
        padding: 9px 15px 9px 5px;
        background: #FFFFFF;
        box-shadow: 0 2px 6px rgba(40, 43, 49, 0.08);
        border-radius: 4px;
    }
    .choose_plan_apply {
        display: flex;
        justify-content: space-between;
    }
    .choose_plan_apply input {
        width: 90px;
        min-height: 40px;
        border: none;
        background: #FFFFFF;
        box-shadow: 0 2px 6px rgba(40, 43, 49, 0.08);
        border-radius: 4px;
    }
    .choose_plan_apply button {
        width: 130px;
        min-height: 40px;
        border: none;
        background: linear-gradient(162.9deg, #7956EC 0%, #2FB9F8 100%);
        border-radius: 6px;
    }
    .choose_plan_apply_input {
        padding: 9px 116px 9px 15px;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 22px;
        color: #676C75;
        mix-blend-mode: normal;
        opacity: 0.5;
    }
    .choose_plan_apply_button {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: bold;
        font-size: 14px;
        line-height: 19px;
        text-align: center;
        letter-spacing: 1px;
        color: #FFFFFF;

    }
    .plan_professional {
        position: absolute;
        width: 350px;
        height: 510px;
        left: 635px;
        top: 968px;
        background-image: url('../../assets/professional_plan_background.png');
        background-repeat: no-repeat;
        box-shadow: 0 6px 12px rgba(32, 33, 39, 0.08);
        border-radius: 12px;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-content: space-around;
        align-items: center;
        z-index: 999;
    }
    .plan_professional div:nth-child(1){
        width: 100%;
        min-height: 39px;
        background: rgba(255, 255, 255, 0.35);
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .plan_professional div:nth-child(1) p {
        width: 350px;
        min-height: 39px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 800;
        font-size: 11px;
        line-height: 15px;
        text-align: center;
        letter-spacing: 2px;
        text-transform: uppercase;
        color: #FFFFFF;
        background: rgba(255, 255, 255, 0.07);
    }
    .plan_professional :nth-child(2) p{
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 300;
        font-size: 60px;
        line-height: 82px;
        text-align: center;
        color: #FFFFFF;
    }
    .plan_professional :nth-child(3) ul {
        width: 220px;
        min-height: 150px;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 15px;
        line-height: 30px;
        color: #FFFFFF;
    }
    .plan_starter :nth-child(3) ul {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 15px;
        line-height: 30px;
        color: #676C75;
    }
    .plan_professional :nth-child(3) ul li, .plan_starter:nth-child(3) ul li {
        display: flex;
        align-items: center;
        list-style: none;
    }
    .plan_professional :nth-child(3) ul li img, .plan_starter:nth-child(3) ul li img {
        margin-right: 7px;
        width: 16px;
        min-height: 12px;
    }
    .plan_professional :nth-child(3) ul li img {
        color: #999EA8;
    }
    .plan_starter :nth-child(3) ul li img {
        color: #282B31;
    }
    .plan_professional div:last-child button {
        width: 250px;
        min-height: 50px;
        border: none;
        background: linear-gradient(168.69deg, #FF8E64 0%, #FFE641 100%);
        border-radius: 6px;
    }
    .plan_buttons{
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: bold;
        font-size: 17px;
        line-height: 23px;
        text-align: center;
        letter-spacing: 1px;
        color: #FFFFFF;
    }

    .plan_starter {
        position: absolute;
        width: 335px;
        height: 470px;
        left: 970px;
        top: 988px;
        background: #FFFFFF;
        box-shadow: 0 1px 3px rgba(32, 33, 39, 0.12);
        border-radius: 12px;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-content: space-around;
        align-items: center;
    }
    .plan_starter div:nth-child(1) {
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 800;
        font-size: 11px;
        line-height: 15px;
        text-align: center;
        letter-spacing: 2px;
        text-transform: uppercase;
        color: #676C75;
        width: 335px;
        min-height: 39px;
        background: #F8F9FA;
        box-shadow: 0 1px 0 #E7E8EA, inset 0 1px 0 #E7E8EA;
    }
    .plan_starter div:nth-child(2) p {
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 300;
        font-size: 40px;
        line-height: 55px;
        text-align: center;
        color: #282B31;
        text-transform: uppercase;
    }
    .plan_starter div:last-child button {
        width: 235px;
        min-height: 50px;
        border: none;
        background: linear-gradient(167.99deg, #009FC5 0%, #3CECB0 100%);
        border-radius: 6px;
    }
</style>