# 祈年殿 AR

## 使用

1. 先打开 `compile-target.html`，点击“生成识别文件”。
2. 下载 `targets.mind`，放到 `assets/targets.mind`。
3. 打开 `index.html`，允许摄像头权限。
4. 摄像头扫描第一张“星河天”图片后，祈年殿模型会出现在右上角圆形柱网位置并原地旋转。

## 本地预览

在本目录运行：

```powershell
python -m http.server 8088
```

然后访问：

```text
http://localhost:8088/compile-target.html
http://localhost:8088/index.html
```

手机测试需要 HTTPS，可以部署到 GitHub Pages，或使用支持 HTTPS 的本地隧道。

## 上传到 GitHub Pages

1. 先用 `compile-target.html` 生成 `assets/targets.mind`。
2. 把整个 `E:\code\tiantan` 文件夹上传到 GitHub 仓库。
3. 在仓库 `Settings` -> `Pages` 中选择从 `main` 分支根目录发布。
4. 发布后访问 GitHub Pages 地址，用手机浏览器打开并允许摄像头权限。

## 资产说明

- `assets/target.png`: 第一张识别图。
- `assets/targets.mind`: MindAR 识别文件，需要先生成后上传。
- `assets/tiantan-centered.obj`: 已居中处理的祈年殿模型，方便围绕自身旋转。
- `assets/tiantan.mtl`: 简化材质文件。原始 MTL 引用了贴图文件夹，但当前目录没有贴图，所以先保留材质颜色。
