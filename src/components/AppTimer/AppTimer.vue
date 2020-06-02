<template>
    <section class="app_timer">

        <AppTimerHeader :change-name="changeName"
                        :timer-name="timerName"
                        :on-enter-press="onEnterPress"
                        :create-item="createItem">
        </AppTimerHeader>
        <AppTimerList :items="items"
                      :save-to-local-storage="saveToLocalStorage"
                      :delete-item="deleteItem"
        ></AppTimerList>
    </section>
</template>
<script>
    import AppTimerHeader from '../AppTimerHeader/AppTimerHeader';
    import AppTimerList from '../AppTimersList/AppTimersList';
    export default {
        data: function(){
            return {
                items: [],
                timerName: '',
                id: 0,
            }
        },
        created: function(){
            if(localStorage.getItem('list-timers')){
                this.items = this.items.concat(JSON.parse(localStorage.getItem("list-timers")));
            }
        },
        methods: {
            changeName(string){
                return this.timerName = string;
            },
            onEnterPress(string){
                this.changeName(string);
                return this.createItem()
            },
            createItem(){
                if(!this.timerName){
                    this.timerName = new Date().toISOString();
                }
                this.items.unshift({id: this.id, name: this.timerName, time: new Date(), isPaused: false});
                this.timerName = '';
                this.id = this.id + 1;
                this.saveToLocalStorage();
                return this.items;
            },
            deleteItem(id){
                this.items.map((elem, i) => {
                    if(elem.id === id) {
                        this.items.splice(i, 1);
                    }
                });
                localStorage.setItem('list-timers', this.items);
                return this.items.map;
            },
            saveToLocalStorage(){
                localStorage.setItem('list-timers', JSON.stringify(this.items));
            }
        },
        components: {
            AppTimerHeader,
            AppTimerList
        },
    }
</script>
<style>
    .app_timer {
        overflow: hidden;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        position: absolute;
        width: 770px;
        height: 421px;
        left: 335px;
        top: 1898px;
        background: #FFFFFF;
        box-shadow: 0 12px 24px rgba(40, 43, 49, 0.16);
        border-radius: 12px;
    }
    @media screen and (max-width: 1400px) and (min-width: 960px) {
        .app_timer {
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            position: absolute;
            width: 65%;
            height: 421px;
            left: 200px;
            top: 2100px;
            background: #FFFFFF;
            box-shadow: 0 12px 24px rgba(40, 43, 49, 0.16);
            border-radius: 12px;
        }
    }
    @media screen and (max-width: 960px) and (min-width: 600px) {
        .app_timer {
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            position: absolute;
            width: 75%;
            height: 421px;
            left: 105px;
            top: 2100px;
            background: #FFFFFF;
            box-shadow: 0 12px 24px rgba(40, 43, 49, 0.16);
            border-radius: 12px;
        }
    }
    @media screen and (max-width: 600px) and (min-width: 300px) {
        .app_timer {
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            position: absolute;
            width: 770px;
            height: 421px;
            left: 335px;
            top: 1898px;
            background: #FFFFFF;
            box-shadow: 0 12px 24px rgba(40, 43, 49, 0.16);
            border-radius: 12px;
        }
    }
</style>