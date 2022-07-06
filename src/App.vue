<template>
  <div id="app">
    <!-- <NetHeader /> -->
    <NetCenter />
    <NetFooter />
  </div>
</template>

<script>
// import NetHeader from './components/NetHeader.vue'
import NetFooter from './components/NetFooter.vue'
import NetCenter from './components/NetCenter.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    // NetHeader,
    NetFooter,
    NetCenter
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
body {
  display: block;
  background: #DADBDC url(./assets/image/wireless/background.png) repeat-x top;
  min-width: 768px;
  font-family: "Microsoft YaHei", "SimHei", "Apple LiGothic Medium";
}

* {
  margin: 0;
  padding: 0;
  border: 0;
}

a {
  text-decoration: none;
}

a {
    color: #AD3B23;
}

a:hover {
  text-decoration: underline;
}

ul {
  list-style: none;
}

.english {
  font-family: Verdana, Geneva, sans-serif;
}

#app {
  /* top: 0;
  width: 100%; */
  /* height: 100%; */
  min-width: 640px;
  min-height: 100%;
  background: #E6E6E6 url(./assets/image/wireless/popup_bg.png) no-repeat top right;
}

#app .greet {
  top: 64px;
  left: 48px;
  width: 512px;
  height: 224px;
  background: #E64E2E url(./assets/image/wireless/popup_greeting.png) no-repeat 30px 46px;
}

#app #center {
  position: relative;
  width: 640px;
  height: 480px;
  background: url(./assets/image/popup_shadow.png) no-repeat 48px 344px;
}

#app .triangle_greet {
  left: 80px;
  top: 288px;
}

#app #info {
  position: absolute;
  top: 32px;
  left: 304px;
  width: 464px;
  height: 304px;
  background: #F2F2F2;
  -webkit-box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 0 4px rgba(0, 0, 0, 0.1);
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
}

#app #info {
  top: 96px;
  left: 176px;
  padding: 32px;
  width: 352px;
  height: 208px;
}

#app .corner {
  position: absolute;
  top: 288px;
  left: 592px;
  border-color: transparent #CCCCCC;
  border-width: 16px 0 0 16px;
}

#app .bar {
  position: absolute;
  top: 304px;
  right: 32px;
  width: 208px;
  height: 80px;
  background: #FFFFFF;
  -webkit-box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0 0 4px rgba(0, 0, 0, 0.1);
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
}

#app #links {
  position: absolute;
  bottom: 32px;
  right: 32px;
  width: 234px;
}

#app .bar {
  position: absolute;
  top: 304px;
  right: 32px;
  width: 208px;
  height: 80px;
  background: #FFFFFF;
  -webkit-box-shadow: 0 0 8px rgb(0 0 0 / 10%);
  -moz-box-shadow: 0 0 4px rgba(0, 0, 0, 0.1);
  box-shadow: 0 0 8px rgb(0 0 0 / 10%);
}

.greet,
#title,
#popup .alert {
  text-indent: -999em;
  overflow: hidden;
}
</style>
