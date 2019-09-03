animation动画 与 transition 不能一同作用于一个节点上，transition会失效，如果需要可以多加一层。

```
<transition-group name="fade-scale">
    <div v-for="i in 9" :key="i" class="abt" :class="'img_txt'+i" v-show="hasNum(i)">
        <div :class="'animation' + i">
            <div class="flow" :class="'flow'+i+'_img'" @click="getDD(i)" ></div>
            <div class="get_txt"></div>
        </div>
    </div>
</transition-group>
```
