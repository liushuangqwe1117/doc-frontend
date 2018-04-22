## video元素介绍
> 视频、影片、带字幕的音频

### 属性
- src：视频URL
- width：显示宽度
- height：显示高度
- poster：视频默认显示的图片URL
- preload：是否预加载视频，如果使用"autoplay"，则忽略该属性
  - auto：当页面加载后载入整个视频
  - meta：当页面加载后只载入元数据
  - none：当页面加载后不载入视频
- autoplay：视频在就绪后马上播放
- loop：当媒介文件完成播放后再次开始播放
- muted：视频的音频输出被静音
- controls：显示视频控制栏
- crossorigin：跨域
- source(src,type)：可以针对不同浏览器加载不同格式的视频文件
  ![](assets/html/images/video1.png)
- track：为视频提供字幕
  - kind(subtitles,captions,descriptions,chapters,metadata)
  - src
  - srclang
  - label
  - default
  ![](assets/html/images/video2.png)
