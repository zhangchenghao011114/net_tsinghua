<template>
    <ul id="links">
        <!-- <li><a id="link_info" href="http://info.tsinghua.edu.cn" target="_new" title="清华信息门户&#10;info.tsinghua">Info</a>
        </li>
        <li><a id="link_lib" href="http://lib.tsinghua.edu.cn/" target="_new" title="清华图书馆&#10;lib.tsinghua">Lib</a>
        </li>
        <li><a id="link_learn" href="http://learn.tsinghua.edu.cn/" target="_new"
                title="清华网络学堂&#10;learn.tsinghua">Learn</a></li>
        <li><a id="link_mail" href="http://mail.tsinghua.edu.cn/" target="_new" title="清华邮箱&#10;mail.tsinghua">Mail</a>
        </li> -->
        <li><a id="link_info" :href="links[0].url" :target="links[0].target" :title="links[0].name" >Info</a></li>
        <li><a id="link_lib" :href="links[1].url" :target="links[1].target" :title="links[1].name">Lib</a></li>
        <li><a id="link_learn" :href="links[2].url" :target="links[2].target" :title="links[2].name">Learn</a></li>
        <li><a id="link_mail" :href="links[3].url" :target="links[3].target" :title="links[3].name">Mail</a></li>
    </ul>
</template>

<script>
export default {
    name: 'NetLinks',
    data(){
        return {
            links: [
                {
                    name: '清华信息门户',
                    url: 'http://info.tsinghua.edu.cn',
                    target: '_new'
                },
                {
                    name: '清华图书馆',
                    url: 'http://lib.tsinghua.edu.cn/',
                    target: '_new'
                },
                {
                    name: '清华网络学堂',
                    url: 'http://learn.tsinghua.edu.cn/',
                    target: '_new'
                },
                {
                    name: '清华邮箱',
                    url: 'http://mail.tsinghua.edu.cn/',
                    target: '_new'
                }
            ]
        }
    }
}
</script>

<style>
#links #link_info {
    background: url(../assets/image/wireless/popup_info.gif) no-repeat 2px 2px;
}

#links #link_lib {
    background: url(../assets/image/wireless/popup_lib.gif) no-repeat 2px 2px;
}

#links #link_learn {
    background: url(../assets/image/wireless/popup_learn.gif) no-repeat 4px 1px;
}

#links #link_mail {
    background: url(../assets/image/wireless/popup_mail.gif) no-repeat 0 1px;
}

#links li {
    float: left;
    margin-right: 12px;
    font-size: 11px;
    font-family: Verdana, Geneva, sans-serif;
}

#links li:last-child {
    float: right;
    margin: 0;
}

#links li a {
    display: block;
    padding: 16px 0 0 26px;
    height: 16px;
}
</style>