
### 技术储备

正式开发前，我们希望你对下面的两点基础知识有所了解：

1. HTML，CSS和JavaScript的基本知识；
2. 对MIP的基础原理和规范，请参考[MIP 的开发文档](/doc/00-mip-101.html) ；

### 开发环境和demo

1、下载代码；

- 下载本教程的代码，下载地址如下：[oscar-demo](http://mipstatic.baidu.com/static/mip-static/mip-story/demo/story-demo.zip)；
- 提取zip文件的内容，减压后在story-demo目录下的oscar-story.html是完整小故事demo的入口。

2、运行示例页面

​&emsp;&emsp;运行示例代码的方法和访问一个MIP页面的方法一样，MIP 页文件可以直接运行，您可以选择如下方式，像预览普通 HTML 文件一样预览 MIP-HTML 页面：

- 直接在浏览器中打开（由于 XML HTTP Requests 失败可能会导致某些元素预览失败）。
- 在本地部署一个服务，如 Apache，Nginx 等。
   使用 MIP-CLI 辅助预览，使用方法见 MIP 博客：[开发教程一](http://www.cnblogs.com/mipengine/p/mip_cli_1_install.html)。

设置完本地的web服务，通过访问一下URL，可查看小故事的Demo示例：

```
http://localhost:8000/oscar-story.html
```

​&emsp;&emsp;完成了以上准备工作，接下来，我们会以这个小故事为例子，来一点点为你讲解如何开发一个小故事。
