下面请跟随详细步骤教程开始制作您的第一个小故事吧！

### 在页面中添加mip-story 组件标签；

​&emsp;&emsp;`mip-story` 是一个自定义的MIP组件，与使用其他MIP组件一样，您必须要将该组件的关联脚本添加到html页面中；在一个标准的 [MIP HTML 页面](/doc/01-mip-demo.html)的`<script>`标签中添加依赖脚本：
  添加好依赖后，需要把`mip-story`元素添加到`<body>`文档中，如下所示：

```html
<!DOCTYPE html>
<html mip>
<head>
    ....
</head>
<body>
    <!-- 组件使用 -->
    <mip-story id="story-demo">
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
接下来我们向这个页面里去填充我们的小故事页面的内容；
首先是封面，我们通常把`<mip-story>`的第一个`<mip-story-view>`子元素乘坐小故事的封面页。
然后通过为这个`<mip-story-view>`元素添加子元素`<mip-story-layer>`的方式来创建图层。为了使封面页的背景图片充满屏幕，可设置`<mip-story-layer>`中的**`template`属性**为`fill`，指定该`template="fill"`。在图层内部，[`<mip-img>`](/examples/mip/mip-img.html)为`cover.jpg`文件添加一个元素，并确保它对`layout="responsive"`图像尺寸为720 x 1280像素的响应。

- 示例：

```html
<mip-story>
    <mip-story-view id="cover">
        <mip-story-layer template="fill">
            <mip-img layout="responsive" width="720" height="1280" src="https://www.mipengine.org/static/img/mip-story/p1.png"></mip-img>
        </mip-story-layer>
    </mip-story-view>
</mip-story>
```
&emsp;&emsp;在完成第一层的背景图之后，需要填充封面页上的内容，如主标题和副标题。

​&emsp;&emsp;在页面中继续添加一个`<mip-story-layer>` 标签，并给他添加子元素主标题和副标题。 为了使这些元素依次排列，需给`<mip-story-layer>`的`template`属性赋值`vertical`。

- 示例：

```html
<mip-story>
    <mip-story-view>
        <mip-story-layer template="fill">
            <mip-img  layout="responsive" width="480" height="720" class="fade-in-scale" src="https://www.mipengine.org/static/img/mip-story/p1.png" layout="responsive"></mip-img>
        </mip-story-layer>
        <mip-story-layer template="vertical">
            <div class="page1-wrap">
                <span>第90届奥斯卡</span>
                <span>The 90th Oscar</span>
                <span class="line"></span>
                <span>颁奖典礼回顾</span>
            </div>
        </mip-story-layer>
    </mip-story-view>
</mip-story>
```

  通过以上代码，可实现完整的小故事封面，图形化界面如下：

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/cover-6.png" width="276" height="494" />
</div>



接下来继续向页面中添加另外的内容元素；


### 添加第一个内容段落

```html
<mip-story>
	<mip-story-view>
		<mip-story-layer template="vertical">
			<!-- 主标题 -->
			<div class="common-wrap">山姆·洛克威尔</div>
			<mip-img layout="responsive" width="1242" height="1665" src="./static/p5.png"></mip-img>
			<!-- 副标题 -->
			<div class="common-wrap-1">
				<span></span>
				<span>最佳男配角</span>
				<span>主演：三块广告牌</span>
			</div>
		</mip-story-layer>
	</mip-story-view>
</mip-story>
```

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/vertical-0.png" width="276" height="494" />
</div>

### 添加第二个内容段落

```html
<mip-story>
    <mip-story-view>
        <mip-story-layer template="fill">
            <mip-img layout="responsive" width="480" height="720" src="https://www.mipengine.org/static/img/mip-story/p6.png"></mip-img>
        </mip-story-layer>
        <mip-story-layer template="thirds" class="common-wrap-2">
            <div flex-area="upper-third">艾莉森·珍妮</div>
            <div flex-area="middle-third"></div>
            <div flex-area="lower-third">
                <span></span>
                <div>最佳女配角</div>
                <div>主演: 我，花样女王</div>
            </div>
        </mip-story-layer>
    </mip-story-view>
</mip-story>
```

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/fill-0.png" width="276" height="494" />
</div>

  以上是分别两种不同形式的，可满足您在开发过程的不同布局需求，完成内容段落之后，接下来，需要去完善一下小故事的封底页面；



## 为小故事添加封底页面

  一个完整的故事需要有一个美好的结局，小故事页面也是一样。我们添加完内容页面之后，在结尾需要设置一个合适的结尾封底页面；

​​​&emsp;&emsp;这个页面我们采用数据配置的方式去完成；

  如下面的代码格式所示，在`<mip-story>`标签下添加一个`<script type="application/json"></script>`来进行这些配置；

### share

```html
<mip-story>
    <script type="application/json">
    {
         "share": {
                "thumbnail": "https://www.mipengine.org/static/img/mip-story/cover.jpg",
                "background": "https://www.mipengine.org/static/img/mip-story/p8.png",
                "title": "第90届奥斯卡颁奖典礼回顾",
                "from": "小故事",
                "desc": "一分钟带你了解第九十届奥斯卡颁奖典礼",
                "readings": "10000"
            }
     }
	</script>
    <mip-story-view>
        <mip-story-layer template="fill">
        </mip-story-layer>
    </mip-story-view>
</mip-story>
```

配置完以上信息，您的封底页面就已经初步完成了；

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/share.png" width="276" height="494" />
</div>

### recommend

​​​&emsp;&emsp;如果您希望用户在阅读完当前的小故事之后，可以看到更多推荐的内容，我们提供了`recommend`字段可继续配置推荐内容的数据。

```html
<mip-story>
    <script type="application/json">
    {
        "share": {
            "thumbnail": "img/share.jpg",
            "background": "img/sharebg.png",
            "title": "相约一起看樱花",
            "desc": "带您了解世界著名的赏樱圣地",
            "from": " "
        },
        "recommend": {
        "url": "",
        "items": [
            {
                "cover": "https://img6.bdstatic.com/img/image/public/ribenshangying3.jpg",
                "url": "http://shxingtuan.com/jp_sakura/index.html",
                "title": "日本赏樱推荐",
                "from": " ",
                "fromUrl": " "
            },
            {
                "cover": "https://img6.bdstatic.com/img/image/public/shangyingmeitu.jpg",
                "url": "https://m.baidu.com/sf/vsearch?pd=image_content&word=%E8%B5%8F%E6%A8%B1&tn=vsearch&sa=vs_tab&lid=9813145669733695291&ms=1&atn=page&fr=tab&ssid=2e3d6e69757a696e616e6e616ece0f",
                "title": "往年樱花美图欣赏",
                "from": " ",
                "fromUrl": " "
            }
        ]
        }
     }
	</script>
    <mip-story-view>
        <mip-story-layer template="fill">
        </mip-story-layer>
    </mip-story-view>
</mip-story>
```

- 示例

<div align=center>
    <img src="http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/share.jpeg" width="276" height="494" />
</div>

