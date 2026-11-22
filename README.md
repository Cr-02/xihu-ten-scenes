# 西湖十景 · 一湖烟雨

课程作业：制作前端网页并在云端部署。
一个整屏不滚动的西湖十景页面——整张实景航拍作底，下方是十景实景缩略图，点开弹出大图与典故卡片。

## 在线地址

- GitHub Pages（国内可直连）：https://cr-02.github.io/xihu-ten-scenes/
- Vercel：https://xihu-ten-scenes.vercel.app/

## 文件结构

```
index.html          页面本体（HTML + CSS + JS 全在这一个文件里，零外部依赖）
credits.json        十张照片的来源、作者与授权
img/                十景实景大图（点击弹窗时加载）
img/t/              对应的缩略图（首屏图墙加载，480×320）
```

## 技术说明

- 纯静态，无构建步骤、无框架、无 CDN 依赖。
- 一屏布局：`height:100dvh` + grid，任何分辨率下都不产生滚动条。
- 图片：Wikimedia Commons，CC BY / CC BY-SA / CC0 授权，作者见 `credits.json`。

## 本地查看

直接双击 `index.html` 即可，不需要起服务器。
