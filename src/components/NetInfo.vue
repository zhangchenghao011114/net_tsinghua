<template>
    <div id="info">
        <h2 class="user_name" id="uname">{{UserName}}</h2>
        <div id="info_content">
            <div class="label_text">已连接<p class="english">Duration</p>
            </div>
            <div class="content_text"><span id="clock" style="color:#ec6677" >{{NetTime}}</span><span class="unit"></span></div>
            <div class="label_text">已用流量<p class="english">Usage</p>
            </div>
            <div class="usage_bar">
                <ul class="calibration">
                    <li>125</li>
                    <li>100</li>
                    <li>75</li>
                    <li>50</li>
                </ul>
                <!-- <div id="usage_value" style="width:69px;"></div> -->
                <div id="usage_value" :style="{width:Usage*2.1+'px'}"></div>
                <div class="stripe"></div>
                <div class="stripe second_stripe"></div>
                <div class="content_text"><span class="unit" id="usage_flux">{{Usage+"G"}}</span></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "NetInfo",
    mounted() {
        this.timer = setInterval(() => {
            this.NetTime = new Date().toLocaleTimeString();
        }, 1000);
    },
    beforeDestroy() {
        if(this.timer) {
            clearInterval(this.timer);
        }
    },
    data(){
        return {
            NetTime: new Date().toLocaleTimeString(),
            UserName: "ch-zhang20",
            Usage: "50",
        }
    },
    computed:{
        usage_len(){
            return this.Usage*2;
        }
    },
}
</script>

<style>

#info .user_name {
    float: left;
    color: #E64E2E;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 34px;
    font-weight: lighter;
}

#info #account {
    float: left;
    margin: 8px 0 0 16px;
    background-position: 2px 4px;
    line-height: 1.1;
}

#info #info_content {
    float: left;
    margin-top: -8px;
}

#info .label_text {
    clear: left;
    float: left;
    width: 56px;
    height: 32px;
    margin-top: 22px;
    text-align: right;
    font-size: 13px;
}

#info .label_text .english {
    font-size: 13px;
}

#info .content_text {
    float: left;
    margin: 24px 0 0 20px;
    padding-top: 4px;
    height: 28px;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 28px;
    font-weight: lighter;
}

#info .content_text .unit {
    margin-left: 8px;
    color: #5C5C5C;
}

#info .usage_bar {
    position: relative;
    float: left;
    margin: 24px 0 0 16px;
    padding: 0;
    width: 280px;
    height: 32px;
    background: url(../assets/image/wired/usage_bg.gif) repeat-y;
}

.usage_bar .stripe {
    position: absolute;
    top: 0;
    right: 4px;
    width: 4px;
    height: 100%;
    background: #F2F2F2;
}

.usage_bar .second_stripe {
    right: 12px;
}

#info .usage_bar .content_text {
    position: absolute;
    top: 2px;
    left: 4px;
    float: none;
    margin: 0;
    padding: 0;
}

.usage_bar .content_text .unit {
    font-size: 24px;
}

.usage_bar .calibration {
    position: absolute;
    top: -16px;
    right: 14px;
    font-family: Verdana, Geneva, sans-serif;
    font-size: 13px;
    color: #969696;
}

.calibration li {
    float: right;
    width: 53px;
    text-align: right;
}

.usage_bar #usage_value {
    float: left;
    height: 32px;
    max-width: 280px;
    background: #FBB03B;
}
</style>