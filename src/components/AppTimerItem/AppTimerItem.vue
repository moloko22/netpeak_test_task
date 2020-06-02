<template>
    <li class="app_timer_item">
    <p>{{item.name}}</p>
    <p :id="item.isPaused ? 'pause_background': 'play_background'">{{formattedTimer}}</p>
    <button v-if="item.isPaused"
            class="play"
            v-on:click='setStart(item.id)'>
        <img
                src="../../assets/play.png"
                alt="start"></button>
    <button v-if="!item.isPaused"
            class="pause"
            v-on:click='setPause(item.id)'>
        <img
                src="../../assets/pause.png"
                alt="pause"></button>
    <button v-on:click='deleteItem(item.id)'
            class="delete">
        <img src="../../assets/delete.png" alt="delete">
    </button>
</li>
</template>
<script>
    export default {
        data: function(){
            return {
                currentTimer: 0,
                formattedTimer: '00:00:00',
                ticker: undefined,
            }
        },
        created: function(){
            this.currentTimer = this.item.currentTimer || 0;
            this.formattedTimer = this.formatTime(this.currentTimer);
            if(!this.item.isPaused){
                this.setStart(this.item.id);
            }
        },
        props: ['item', 'deleteItem', 'saveToLocalStorage'],
        methods: {
            setStart(){
                this.item.isPaused = false;
                this.saveToLocalStorage();
                this.tick();
            },
            setPause(){
                clearInterval(this.ticker);
                this.item.isPaused = true;
                this.saveToLocalStorage();
            },
            tick(){
                this.ticker = setInterval(() => {
                    this.currentTimer++;
                    this.formattedTimer = this.formatTime(this.currentTimer);
                    this.item.currentTimer = this.currentTimer;
                    this.saveToLocalStorage();
                }, 1000)
            },
            formatTime(seconds){
                let measuredTime = new Date(null);
                measuredTime.setSeconds(seconds);
                let MHSTime = measuredTime.toISOString().substr(11, 8);
                return MHSTime;
            }
        }

    }
</script>
<style>
    #pause_background {
        border: none;
        background: rgba(255, 72, 118, 0.15);
        border-radius: 6px;
    }
    #play_background{
        background: #E7E8EA;
        border: 1px solid #E7E8EA;
        box-sizing: border-box;
        border-radius: 6px;
        border: none;

    }
    .pause {
        background: linear-gradient(135deg, #7956EC 0%, #2FB9F8 100%);
        border-radius: 25px;
        width: 50px;
        min-height: 50px;
        border: none;
    }
    .play {
        width: 50px;
        min-height: 50px;
        border: none;
        background: linear-gradient(135deg, #009FC5 0%, #3CECB0 100%);
        border-radius: 25px;
    }
    .pause img, .play img, .delete img{
        width: 30px;
        min-height: 25px;
    }
    .delete {
        width: 50px;
        min-height: 50px;
        border: none;
        background: linear-gradient(135deg, #F23673 0%, #FCA069 100%);
        border-radius: 6px;
    }
    .app_timer_item {
        margin-bottom: 40px;
        width: 100%;
        min-height: 50px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .app_timer_item p:nth-of-type(1){
        min-width: 80px;
        max-width: 180px;
        overflow: hidden;
        text-overflow: ellipsis;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: 800;
        font-size: 20px;
        line-height: 30px;
        color: #5586F2;
    }
    .app_timer_item p:nth-of-type(2){
        width: 117px;
        min-height: 50px;
        background: #E7E8EA;
        border: 1px solid #E7E8EA;
        box-sizing: border-box;
        border-radius: 6px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: Nunito Sans;
        font-style: normal;
        font-weight: normal;
        font-size: 17px;
        line-height: 23px;

        color: #676C75;
    }
</style>