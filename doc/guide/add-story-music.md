我们可以通过给小故事页面添加背景音乐和视频的形式来增加页面的趣味性。

### 为小故事添背景音乐

在一个小故事页面中，你可以有两种方式来添加背景音乐；

#### 添加全局的背景音乐

​​&emsp;&emsp;我们通过给`mip-story` 标签添加 `background-audio` 属性来为小故事页面添加全局的背景音乐；

```html
<mip-story background-audio="您的音乐地址链接">
    <mip-story-view>
        <mip-story-layer template="fill">
        </mip-story-layer>
    </mip-story-view>
</mip-story>
```

#### 为小故事的段落页面添加背景音乐

​​&emsp;&emsp;除了添加全局的背景音乐之外，您还可以针对具体的小故事段落添加独立的背景音乐；
我们通过给`mip-story-view` 标签添加 `background-audio` 属性来完成这一操作；

```html
<mip-story>
    <mip-story-view background-audio="您的音乐地址链接">
        <mip-story-layer template="fill">
        </mip-story-layer>
    </mip-story-view>
</mip-story>
```

注意：如果您添加了全局背景音乐，那么将会默认播放全局的背景音乐，针对段落添加的背景音乐将不会生效；

### 为小故事页面添加视频


