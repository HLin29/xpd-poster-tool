# XPD 海报智能制作工具

## 功能简介

一个用于制作 XPD 流程宣传海报的在线工具，支持：
- 🎨 多种海报类型（功能宣传 / 对话气泡 / 飞书消息卡片 / 自由创作）
- 🤖 AI 文案生成（支持 Gemini 3 Pro 和 QoderWork AI 双模式）
- 📋 一键生成 VisionX 做图 Prompt
- 📚 历史记录保存（localStorage 持久化）
- 📦 案例模板一键加载
- 💾 历史记录导出/导入

## 部署说明

本项目部署到 **GitHub Pages**，免费、无服务器、无需域名。

### 一键部署步骤

#### 1. 创建 GitHub 仓库

访问 https://github.com/new ，填写：
- **Repository name**: `xpd-poster-tool`
- **Public**（GitHub Pages 需要公开仓库）
- 点击 **Create repository**

#### 2. 上传文件

方法A - 网页上传：
1. 在仓库页面点击 **Add file > Upload files**
2. 把本目录下的 `index.html` 拖入上传区域
3. 点击 **Commit changes**

方法B - 命令行上传：
```bash
git init
git remote add origin https://github.com/你的用户名/xpd-poster-tool.git
git add index.html
git commit -m "deploy: XPD poster tool"
git branch -M main
git push -u origin main
```

#### 3. 开启 GitHub Pages

1. 进入仓库 **Settings > Pages**
2. 在 **Source** 选择 **Deploy from a branch**
3. 在 **Branch** 选择 **main**，目录选择 **/(root)**
4. 点击 **Save**

#### 4. 获取在线链接

等待 1-3 分钟，访问：

```
https://你的用户名.github.io/xpd-poster-tool/
```

把这个链接发给同事，任何人都可以直接在浏览器中使用。

## 使用方式

1. **打开链接** → 直接浏览器打开在线地址
2. **Step 0：项目配置** → 选择海报类型、填写基础信息
3. **Step 1：AI 方案生成** → 选择 Gemini 3 Pro 或 QoderWork AI 模式
4. **Step 2：VisionX 做图 Prompt** → 自动根据 AI 方案生成精确 Prompt
5. **Step 3：修改优化** → 勾选问题、补充说明，生成修改 Prompt

## 技术架构

- 纯静态 HTML（单文件，无服务器）
- 历史记录使用 localStorage 持久化
- 所有 CDN 资源使用外部链接（Google Fonts、Tailwind CSS、FontAwesome）

## 更新工具

当有新版本的工具时：
1. 下载新的 `index.html`
2. 替换仓库中的文件
3. GitHub Pages 会自动更新（1-3分钟）

## 内部网络访问

如果公司内网无法访问 GitHub Pages，可以考虑：
- 部署到腾讯云 COS / 阿里云 OSS
- 部署到公司内部静态托管服务器
- 直接通过飞书文档/文件分享给同事
