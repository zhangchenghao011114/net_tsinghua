<template>
    <div id="NetHead">
        <div id="head">
            <a id="title" href="" title="清华大学校园网
Tsinghua University Network"></a>
        </div>
        <div class="f-img">
            <img src="../assets/image/qr.jpg">
            <p>欢迎关注"清华大学信息服务"</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "NetHeader",
};
</script>

<style>
#head {
    float: left;
    margin: 16px 0 32px -48px;
    background: url(../assets/image/wired/logo.gif) no-repeat;
}
.f-img {
    float: right;
    margin-top: 30px;
    text-align: center;
}
</style>