

​正式开发前，我们先来了解一下一个小故事页面的组织结构。

## 小故事的组织结构介绍

​&emsp;&emsp;小故事主要由 [mip-story 组件](/examples/mip-extensions/mip-story.html) 承载，充当小故事中所有段落的容器，按照段落个数自动生成段落导航，段落播放完的重播和分享功能。

小故事具有三个基本概念：段落（view），层（layer）和元素（element）.

- 每个小故事可以包含多个段落（view），每个段落充满屏幕。用户操作翻页后，会看到下一个段落。
- 每个段落又可以包含多个层（layer），单个层可以设置布局模式，如多行布局，左右布局，图片拉伸布局等。
- 元素（element）是资源素材，如背景图，主标题，详细描述等。在 `<h1>`、`<p>`、`<mip-img>` 等标签中声明。

![intro-view-layer-element (1)](http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/intro-view-layer-element.jpg)

​&emsp;&emsp;这里的每一个元素都是一个mip组件，其中故事组件 为`mip-story`，段落为`mip-story-view`，层为`mip-story-layer`，元素为资源素材，如背景图，主标题，详细描述等。在 `<h1>`、`<p>`、`<mip-img>` 等标签中声明。



![mip-story-tag-hierarchy](http://mipstatic.baidu.com/static/mip-static/mip-story/demo/static/demo-story1.png)
