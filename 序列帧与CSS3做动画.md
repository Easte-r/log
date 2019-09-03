## 使用序列帧做动画

遇到过一个产品动画需求，使用GIF后资源大，且清晰度不高。从腾讯lol官网得到的灵感，他们的网站banner动画使用的就是15张图拼接成的序列帧。
使用animation 的steps动画函数进行序列帧的移动。

合成雪碧图 （https://www.toptal.com/developers/css/sprite-generator ）
压缩png （https://compresspng.com/zh/ ）


@keyframes animation {
    100%{background-position:-367.5rem 0 }
}

animation: animation 2s steps(49, end) infinite;

示例地址：
    - https://lpl.qq.com/es/worlds/2018/
