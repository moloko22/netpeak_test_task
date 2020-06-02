<template>
    <div class="app_timer_header">
        <label>
            <input type="text"
                   placeholder="Timer Name"
                   v-bind:value="timerName"
                   v-on:keydown="(e) => onKeyDown(e)"
                   v-on:input ="(e) => onChange(e.target.value)">
        </label>
        <button v-on:click="createItem()"
                class="app_timer_header_button"
        >Create Timer</button>
    </div>
</template>
<script>
    export default{
        data: function(){
            return {
                name: '',
            }
        },
        props: ['changeName', 'createItem', 'timerName', 'onEnterPress'],
        methods: {
            onChange(str){
                this.name = str;
                this.changeName(this.name);
            },
            onKeyDown(event){
                if(event.keyCode == 13){
                    return this.onEnterPress(event.target.value);
                }
            }
        }
    }
</script>
<style>
    .app_timer_header {
        position: absolute;
        width: 490px;
        height: 50px;
        left: 140px;
        top: 40px;
        display: flex;
        justify-content: space-between;
    }
    .app_timer_header input {
        width: 305px;
        min-height: 50px;
        padding: 14px 192px 11px 20px;
        background: #F8F9FA;
        border: 1px solid #E7E8EA;
        box-sizing: border-box;
        border-radius: 6px;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 17px;
        line-height: 23px;
        color: rgba(103, 108, 117, 0.7);
    }
    .app_timer_header_button {
        width: 113px;
        min-height: 24px;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: bold;
        font-size: 17px;
        line-height: 24px;
        text-align: center;
        letter-spacing: 1px;
        color: #FFFFFF;

    }

    .app_timer_header button {
        width: 165px;
        min-height: 50px;
        background: linear-gradient(163.14deg, #FF8E64 0%, #FFE641 100%);
        border-radius: 6px;
        border: none;
    }
    .app_timer_header :after {
        position: absolute;
        height: 2px;
        background: #E7E8EA;
        width: 100%;
        margin-left: 15px;
        left: 0;
        right: 0;
        top: 100%;
        bottom: 71.26%;
    }
</style>