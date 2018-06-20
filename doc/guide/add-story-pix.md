
​​​&emsp;&emsp;完成了一个小故事开发之后，在正式对外发布之前，可能需要对整个小故事页面添加一些统计埋点，以便后期获取到访问小故事页面的用户行为。在这里我们需要引入统计组件来进行统计。

### 统计页面访问PV

​​&emsp;&emsp;使用 `mip-pix`组件来统计页面访问PV；`mip-pix`组件本身在页面不可见，但本元素只有滚动到屏幕可见范围内才触发初始化;

- 示例

```html
<mip-pix src="https://www.mipengine.org/a.gif"></mip-pix>
```

​​&emsp;&emsp;可以点击[mip-pix 组件](/examples/mip/mip-pix.html)了解更多使用信息。

### 统计用户的交互行为

​​&emsp;&emsp;使用 `mip-stats-baidu` 组件统计用户的交互行为

```html
<mip-stats-baidu>
    <script type="application/json">
        {
            "token": "02890d4a309827eb62bc3335b2b28f7f",
            "_setCustomVar": [1, "login", "1", 2],
            "_setAutoPageview": [true]
        }
    </script>
</mip-stats-baidu>
```

​​&emsp;&emsp;可以点击[ `mip-stats-baidu` 组件](/examples/mip-extensions/mip-stats-baidu.html)介绍了解更多使用信息。完成统计添加，现在可以把您的小故事页面发布到的服务器上让大家浏览了。如果您希望您的小故事页面可以被提交到搜索并被搜索缓存，就必须要通过代码规范校验。
