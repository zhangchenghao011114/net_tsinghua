<template>
    <div class="bar">
        <button class="disconnect">断开连接&nbsp;Disconnect</button>
    </div>
</template>

<script>
export default {
    name: 'NetBar',
}
</script>

<style>
input[type=submit], button {
    text-indent: -999em;
    overflow: hidden;
    cursor: pointer;
    -webkit-appearance: none;
    -moz-appearance: none;
    border-radius: 0;
    -webkit-border-radius: 0;
    -moz-border-radius: 0;
}

.disconnect {
    margin: 16px;
    width: 174px;
    height: 46px;
    border: #B2AABE solid 1px;
    background: #C0BDCC url(../assets/image/disconnect.png) no-repeat center 0;
    overflow: hidden;
}

.disconnect:hover {
    background-color: #D6D2E0;
    background-position: center -47px;
}

.disconnect:active {
    background-color: #B1AAC4;
    background-position: center -94px;
}

.disconnect:disable {
    background-color: #CFCFCF;
    background-position: center -141px;
}
</style>