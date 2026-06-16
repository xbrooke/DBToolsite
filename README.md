# DBTOOL 官网

DBTOOL 2.0 官方网站 - **Apple HIG 风格** 静态站。
纯白 / 浅灰配色、SF 字体栈、毛玻璃导航、pill 按钮、hairline 分隔。
不使用渐变（除 Hero 标题文字色）、不使用 Emoji、不使用位图图标 —— 全部用排版层级与几何 chip 表达信息。

## 文件结构

```
website/
├── index.html            # 单页官网
├── assets/
│   └── styles.css        # 全部样式
├── img/                  # 第三方音乐 App iOS 图标
├── apk/                  # APK 安装包
├── package.json          # 仅提供本地预览脚本
└── README.md             # 本文件
```

## 本地预览

```bash
cd website
npx --yes serve@14.2.3 -l 5173 .
# 浏览器打开 http://127.0.0.1:5173
```

## 部署

任意静态托管即可：GitHub Pages / Netlify / Vercel / Cloudflare Pages / 阿里云 OSS / 腾讯云 COS。
直接上传 `website/` 目录即可上线。

## 设计语言要点

- **颜色**：`#ffffff` 主背景 + `#f5f5f7` 浅灰分区 + `#1d1d1f` 主文字 + `#6e6e73` 次级文字 + `#0071e3` Apple Blue 强调 + `#5A45D6` 紫蓝渐变。
- **字体**：`-apple-system, BlinkMacSystemFont, "SF Pro Text", "PingFang SC", ...`
- **形状**：所有按钮采用 980px 圆角（pill），卡片用 12/18/24px 圆角，分隔线为 1px hairline。
- **动效**：滚动渐入（IntersectionObserver）、按钮按下 scale(0.985)、卡片 hover 上浮、滚动后导航切换为不透明底。
- **可访问性**：所有交互元素带 `:focus-visible` 蓝色描边，FAQ 用原生 `<details>` 获得键盘支持。
