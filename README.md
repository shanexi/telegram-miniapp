# Telegram Mini App Demo

这是一个简单的 Telegram Mini App 演示项目，展示了如何创建和部署一个半屏显示的 Telegram 小程序。

## 功能特性

- 🎨 自适应 Telegram 主题色彩
- 📱 半屏显示模式
- 👤 显示用户信息
- 🔘 主按钮交互
- ⚡ 简单易懂的 Demo 界面

## 本地开发

1. 克隆项目到本地
2. 运行本地服务器：
   ```bash
   npm run dev
   ```
3. 在浏览器中访问 `http://localhost:3000`

## 部署

### 使用 Vercel 部署

1. 将代码推送到 GitHub 仓库
2. 在 Vercel 中导入项目
3. 部署完成后获取 URL

### 使用 Netlify 部署

1. 将代码推送到 GitHub 仓库
2. 在 Netlify 中连接 GitHub 仓库
3. 部署完成后获取 URL

## Telegram Bot 配置

1. 创建 Telegram Bot（如果还没有）
2. 使用 BotFather 设置 Mini App：
   ```
   /setmenubutton
   选择你的 Bot
   输入按钮文本（如："打开应用"）
   输入 Mini App URL（部署后的 URL）
   ```

## 项目结构

```
telegram-miniapp/
├── index.html          # 主页面
├── package.json        # 项目配置
├── vercel.json         # Vercel 部署配置
└── README.md          # 项目说明
```

## 技术栈

- HTML5 + CSS3 + JavaScript
- Telegram Web App SDK
- 响应式设计

## 注意事项

- Mini App 必须部署到 HTTPS 域名
- 确保设置了正确的 CSP 头部允许在 Telegram 中嵌入
- 测试时需要在 Telegram 客户端中打开