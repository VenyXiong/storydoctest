

## 使用小故事内置动画

​​&emsp;&emsp;为了小故事页面更生动，您可以为页面上的元素添加一些入场动画。

- 示例：

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/animation3.gif" width="276" height="494" />
</div>

​​&emsp;&emsp;`mip-story`组件中已封装好了一些常用的动画类型，可以通过给页面元素添加 `animate-in` 属性来进行入场元素动画的设置；

```html
<style mip-custom>
    mip-story-view {
        color: #fff;
    }
    h1 {
        text-align: center;
    }
    .box {
        width: 100px;
        height: 100px;
        background-color: #09f;
        margin-top: 30px;
        margin-left: auto;
        margin-right: auto;
    }
    </style>
<mip-story>
    <mip-story-view>
        <mip-story-layer template="vertical">
            <h1>fade-in</h1>
            <!-- 内置动画的使用方式如下 -->
            <div animate-in="fade-in" class="box"></div>
        </mip-story-layer>
	</mip-story-view>
</mip-story>
```

在小故事的框架中，我们提供了以下预设动画：

| animate-in        | 说明     |
| ----------------- | ------ |
| `fade-in`         | 淡入     |
| `fly-in-top`      | 上侧飞入   |
| `fly-in-bottom`   | 下侧飞入   |
| `fly-in-left`     | 左侧飞入   |
| `fly-in-right`    | 右侧飞入   |
| `fade-in-top`     | 上侧淡入  |
| `fade-in-bottom`  | 下侧淡入  |
| `fade-in-left`    | 左侧淡入  |
| `fade-in-right`   | 右侧淡入  |
| `twirl-in`        | 旋转进入   |
| `whoosh-in-left`  | 左侧放大飞入 |
| `whoosh-in-right` | 右侧放大飞入 |
| `rotate-in-left`  | 左侧旋转飞入 |
| `rotate-in-right` | 右侧旋转飞入 |



- 示例：

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/%E5%B0%8F%E6%95%85%E4%BA%8B%E5%86%85%E7%BD%AE%E5%8A%A8%E7%94%BB.gif" width="276" height="494" />
</div>


### 动画的使用案例

​​&emsp;&emsp;首先可通过以下代码实现一个静态页面。

```html
<mip-story-view>
    <mip-story-layer template="fill">
        <mip-img  layout="responsive" width="480" height="720" src="https://www.mipengine.org/static/img/mip-story/p7.png"></mip-img>
    </mip-story-layer>
    <mip-story-layer>
        <div class="common-wrap1">
            <span></span>
            <span>最佳动画短片</span>
            <span>亲爱的篮球</span>
            <span></span>
            <span>最佳动画长片</span>
            <span>寻梦环游记</span>
        </div>
    </mip-story-layer>
    <mip-story-layer>
        <div class="mask"></div>
    </mip-story-layer>
</mip-story-view>
```

- 示例：

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/animation-0.png" width="276" height="494" />
</div>

​​&emsp;&emsp;在此基础上添加动画，为了使得页面生动，可以添加动画效果。首先制作文本的入口动画，使其在页面中展现淡入的动画效果，像这样添加`animate-in="fade-in"`到`<span>`元素：

```html
<mip-story-view>
    <mip-story-layer template="fill">
        <mip-img  layout="responsive" width="480" height="720" class="fade-in-scale" src="https://www.mipengine.org/static/img/mip-story/p7.png"></mip-img>
    </mip-story-layer>
    <mip-story-layer>
        <div class="common-wrap1">
            <span></span>
            <span animate-in="fade-in" id="sixth-animation">最佳动画短片</span>
            <span>亲爱的篮球</span>
            <span></span>
            <span>最佳动画长片</span>
            <span>寻梦环游记</span>
        </div>
    </mip-story-layer>
    <mip-story-layer>
        <div class="mask"></div>
    </mip-story-layer>
</mip-story-view>
```

​​&emsp;&emsp;接下来，给每个图片添加动画。

```html
<mip-story-view>
    <mip-story-layer template="fill">
        <mip-img  layout="responsive" width="480" height="720" class="fade-in-scale" src="https://www.mipengine.org/static/img/mip-story/p7.png"></mip-img>
    </mip-story-layer>
    <mip-story-layer>
        <div class="common-wrap1">
            <span></span>
            <span animate-in="fade-in" id="sixth-animation">最佳动画短片</span>
            <span animate-in="fly-in-left" animate-in-duration=400 animate-in-after="sixth-animation">亲爱的篮球</span>
            <span></span>
            <span animate-in="fade-in" id="sixth-animation">最佳动画长片</span>
            <span animate-in="fly-in-right" animate-in-duration=400 animate-in-after="sixth-animation">寻梦环游记</span>
        </div>
    </mip-story-layer>
    <mip-story-layer>
        <div class="mask"></div>
    </mip-story-layer>
</mip-story-view>
```
- 示例：

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/animation3.gif" width="276" height="494" />
</div>

## 使用css动画

​​&emsp;&emsp;当然，内置的动画在某些场景下无法完全满足需求，因此，我们也兼容传统的css aniamtion属性动画，您可以在页面中`<style mip-custom></style>` 中定义您的css animation, 并在元素中使用；

[notice] 由于customElement在IOS 11.3上的css animation 存在些兼容性问题，直接使用css动画可能会导致部分情况下动画第一帧丢失，这个问题我们正在解决中。您可以通过显示的为`mip-story`组件声明`display`属性来避免这个问题；


```html
<!DOCTYPE html>
<html mip>
<head>
    <meta charset="utf-8">
    <title>小故事内置动画效果示意图</title>
    <meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1,user-scalable=no">
    <link rel="stylesheet" type="text/css" href="https://mipcache.bdstatic.com/static/v1/mip.css">
    <link rel="canonical" href="http://www.1905.com/mip/oscar">
    <style mip-custom>
		mip-story {
          	display:none;
		}
    </style>
</head>
<body>
    <mip-story>
        ...
	</mip-story>
    <!-- MIP 运行环境 -->
    <script src="https://c.mipcdn.com/static/v1/mip.js"></script>
    <!-- 小故事依赖脚本 -->
    <script src="https://c.mipcdn.com/static/v1/mip-share/mip-share.js"></script>
    <script src="https://c.mipcdn.com/static/v1/mip-story/mip-story.js"></script>
    <script src="https://c.mipcdn.com/static/v1/mip-stats-baidu/mip-stats-baidu.js"></script>
    <script src="https://c.mipcdn.com/static/v1/mip-scrollbox/mip-scrollbox.js"></script>
</body>
</html>
```
