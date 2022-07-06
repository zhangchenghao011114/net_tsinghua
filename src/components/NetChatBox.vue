<template>
    <div id="ChatBox">
        <div class="greet" v-text="msg"></div>
        <div class="triangle_greet"></div>
        <div class="corner"></div>
    </div>
</template>

<script>
export default {
    name: 'NetChatBox',
    data() {
        return {
            msg: '欢迎， ;Welcome,',
        }
    }
};
</script>

<style>
.corner,
.triangle_greet,
.triangle_login,
.triangle_head {
    width: 0;
    height: 0;
    border-style: solid;
}

.greet {
    position: absolute;
    top: 0;
    left: 0;
    width: 720px;
    height: 304px;
    background: #E64E2E url(../assets/image/wireless/popup_greeting.png) no-repeat 32px 28px;
    -webkit-box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
    -moz-box-shadow: 0 0 4px rgba(0, 0, 0, 0.1);
    box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
}

.triangle_greet {
    position: absolute;
    top: 304px;
    left: 32px;
    border-color: #E64E2E transparent;
    border-width: 48px 48px 0 0;
}
</style>