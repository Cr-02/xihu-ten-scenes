# 西湖十景 · 一湖烟雨

课程作业：制作前端网页并在云端部署。
整屏不滚动的西湖十景地图：卫星影像做底，十个景点按真实经纬度标在图上，点标记弹出实景大图与典故。

## 在线地址

- GitHub Pages（国内可直连）：https://cr-02.github.io/xihu-ten-scenes/
- Vercel：https://xihu-ten-scenes.vercel.app/

## 文件结构

```
index.html          页面本体（HTML + CSS + JS 全在一个文件里，零外部依赖）
credits.json        底图与十张实景照片的来源、作者与授权
img/base.jpg        西湖卫星底图（2786×1567，高德 z16 瓦片拼接）
img/<景点>.jpg       十景实景大图，点标记时加载
```

## 技术说明

- 纯静态，无构建步骤、无框架、无 CDN 依赖。
- 一屏布局：`height:100dvh` + grid，任何分辨率下都不产生滚动条。
- 标注精度：景点用 WGS84 经纬度，经 GCJ-02 换算后按 Web Mercator 投影落到像素上，标点与底图严格对应。
- 底图：高德卫星影像，缩放级别 16，按需求区域拼接后重采样。

## 本地查看

双击 `index.html` 即可，不需要起服务器。
