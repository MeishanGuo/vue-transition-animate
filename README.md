### 自定义动画
Vue中可以对使用v-for， v-if， v-show的元素使用动画transition
通过和animate.css动画库的结合，自定义了多种类型的动画：

```
slide：slideLR, slideRL, slideUD, slideDU
fade: fadeLR, fadeRL, fadeUD, fadeDU
bounce: bounceLR, bounceRL, bounceUD, bounceDU
flip: flipX, slipY
lightSpeed: lightSpeedIn, lightSpeedOut
roll: rollIn, rollOut
zoom: zoomIn, zoomOut
*其中，L: left*
*      R: right*
*      U: up*
*      D: down*
分别可以实现相应元素在进入或删除时的动画效果，后续动画类型还会继续扩展
```

### 使用

```
在使用动画时，在需要使用动画的元素上加入animated类，
同时设定该元素的transition属性为上面的一种即可。
```
### 动画钩子函数

```
在methods选项中可以定义以下集中动画钩子函数，分别在动画的几个不同阶段执行：
transitionBeforeEnter
transitionEnter
transitionAfterEnter
transitionEnterCancelled
transitionBeforeLeave
transitionLeave
transitionAfterLeave
transitionLeaveCancelled
```

### 例子

```
<div class="animated" transition="slideLR" v-show="某个条件">
表示：该div元素在插入删除的动画是：从左边slide进入，从右边slide退出

```


### 安装

```
如下‘FILE_PATH’代表vue.directive.check的文件路径
// 全局
<script src="FILE_PATH"></script>
Vue.use(VueDirectiveCheck, options)

// AMD
define([FILE_PATH], function(VueDirectiveCheck){
    Vue.use(VueDirectiveCheck, options)
})
require([FILE_PATH], function(VueDirectiveCheck){
    Vue.use(VueDirectiveCheck, options)
})

// CommonJS
var VueDirectiveCheck = require(FILE_PATH)
Vue.use(VueDirectiveCheck, options)

// ES6
import VueDirectiveCheck from FILE_PATH
Vue.use(VueDirectiveCheck, options)

```
### 示例运行

```
运行环境：python2.7, Flask, npm
进入examples目录执行python demorun.py
```

