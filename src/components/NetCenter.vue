<template>
    <div id="center">
        <NetChatBox />
        <NetInfo />
        <NetBar />
        <NetLinks />
    </div>
</template>

<script>
import NetLinks from './NetLinks.vue'
import NetInfo from './NetInfo.vue'
import NetChatBox from './NetChatBox.vue'
import NetBar from './NetBar.vue'
export default {
    name: 'NetCenter',
    components: {
        NetLinks,
        NetInfo,
        NetChatBox,
        NetBar
    }
}
</script>

<style>
#center {
    margin: auto;
    width: 768px;
    height: 100%;
}
</style>