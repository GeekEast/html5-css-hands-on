## 多媒体标签
- 浏览器兼容性的问题，需要用`<source>`提供ogg和mp3两种格式

### 音频
- `默认`: 不显示**播放控件**
- `controls：` 显示**播放控件**
- `autoplay：` `自动播放`
- `loop`: `循环播放`
```html
    <!-- loop twice -->
    <audio controls autoplay loop="2">
            <source src="horse.ogg">
            <source src="horse.mp3">
            您的浏览器不支持播放改格式的声音文件
    </audio>
```

### 视频
```html
    <video controls width="500" height="300">
        <source src="./play.ogg"></source>
        <source src="./play.mpeg"></source>
        <source src="./play.ogg"></source>
        您的浏览器不支持播放该格式的视频文件
    </video>
```



