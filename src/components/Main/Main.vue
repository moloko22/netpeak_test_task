<template>
    <main>
        <Plan></Plan>
    </main>
</template>
<script>
    import Plan from "@/components/Plan/Plan";
    export default {
        components: {
            Plan,
        }
    }
</script>
<style>
    main{
        width: 100%;
        min-height: 1560px;
        display: flex;
        flex-direction: column;
    }
</style>