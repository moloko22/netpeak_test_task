<template>
    <div class="app_timer_list">
        <ul>
            <AppTimerItem v-for="item in items"
                          :item="item"
                          :save-to-local-storage="saveToLocalStorage"
                          v-bind:key="item.id"
                          :delete-item="deleteItem"
            ></AppTimerItem>
        </ul>
    </div>
</template>
<script>
    import AppTimerItem from "@/components/AppTimerItem/AppTimerItem";
    export default {
        props: ['items', 'obj', 'deleteItem', 'saveToLocalStorage'],
        components: {
            AppTimerItem,
        }
    }
</script>
<style>
    .app_timer_list {
        width: 467px;
        min-height: 500px;
        position: absolute;
        left: 18.18%;
        right: 21.17%;
        top: 35.87%;
        bottom: 52.26%;
        display: flex;
        flex-direction: column;
        align-content: space-around;
    }
    @media screen and (max-width: 1400px) and (min-width: 960px) {

    }
    @media screen and (max-width: 960px) and (min-width: 600px) {
        .app_timer_list {
            width: 467px;
            min-height: 500px;
            position: absolute;
            left: 30px;
            right: 21.17%;
            top: 35.87%;
            bottom: 52.26%;
            display: flex;
            flex-direction: column;
            align-content: space-around;
        }
    }
</style>