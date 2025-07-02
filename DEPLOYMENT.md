# 🚀 Netlify部署指南

## 📋 部署前准备

### 1. 文件清单
确保以下文件都在 `netlify-deploy` 文件夹中：

```
netlify-deploy/
├── protected_chapter_splitter_ai.html  # 主工具页面（受密码保护）
├── password_generator.html             # 动态密码生成器
├── sample_novel.txt                    # 示例小说文件
├── sample_markdown_novel.txt           # 示例Markdown格式小说文件
├── 双处理功能使用说明.md               # 功能说明文档
├── 双处理功能演示.md                   # 演示文档
├── README.md                           # 项目说明
└── DEPLOYMENT.md                       # 本部署指南
```

### 2. GitHub仓库准备
1. 在GitHub上创建一个新的仓库
2. 将 `netlify-deploy` 文件夹中的所有文件上传到仓库根目录
3. 确保仓库是公开的（Netlify免费版需要）

## 🌐 Netlify部署步骤

### 步骤1：注册Netlify账户
1. 访问 [netlify.com](https://netlify.com)
2. 点击 "Sign up" 注册账户
3. 选择 "Sign up with GitHub" 使用GitHub账户登录

### 步骤2：连接GitHub仓库
1. 登录Netlify后，点击 "New site from Git"
2. 选择 "GitHub" 作为Git提供商
3. 授权Netlify访问你的GitHub账户
4. 选择包含部署文件的仓库

### 步骤3：配置部署设置
1. **Branch to deploy**: 选择 `main` 或 `master`
2. **Base directory**: 留空（因为文件在根目录）
3. **Build command**: 留空（静态文件无需构建）
4. **Publish directory**: 留空（文件在根目录）

### 步骤4：部署
1. 点击 "Deploy site"
2. 等待部署完成（通常需要1-2分钟）
3. 部署成功后，你会得到一个类似 `https://random-name.netlify.app` 的URL

## 🔧 高级配置

### 自定义域名
1. 在Netlify控制台中，进入你的站点设置
2. 点击 "Domain settings"
3. 点击 "Add custom domain"
4. 输入你的域名并按照提示配置DNS

### 环境变量（可选）
如果需要配置环境变量，可以在Netlify的 "Site settings" > "Environment variables" 中添加。

## 📱 使用说明

### 访问工具
1. 访问你的Netlify站点URL
2. 点击 `password_generator.html` 获取今日密码
3. 点击 `protected_chapter_splitter_ai.html` 使用主工具
4. 输入今日密码进入工具

### 功能测试
1. 使用 `sample_novel.txt` 测试基本拆分功能
2. 使用 `sample_markdown_novel.txt` 测试Markdown格式
3. 配置AI API密钥测试AI功能

## 🔐 安全注意事项

### 密码保护
- 动态密码每天都会变化
- 密码生成算法基于当前日期
- 建议定期更换密码生成器的盐值

### 访问控制
- 工具完全在客户端运行，数据不会上传到服务器
- 所有文件处理都在用户浏览器中完成
- 建议在HTTPS环境下使用

## 🛠️ 故障排除

### 部署失败
1. 检查GitHub仓库是否公开
2. 确认文件路径正确
3. 检查文件编码是否为UTF-8

### 页面无法访问
1. 检查Netlify部署状态
2. 确认文件已正确上传
3. 检查浏览器控制台是否有错误

### 功能异常
1. 确认浏览器支持现代JavaScript
2. 检查网络连接
3. 尝试清除浏览器缓存

## 📞 技术支持

如果遇到部署问题：
1. 检查Netlify部署日志
2. 查看浏览器开发者工具的错误信息
3. 确认所有文件都已正确上传

## 🔄 更新部署

当你需要更新工具时：
1. 修改本地文件
2. 提交到GitHub仓库
3. Netlify会自动重新部署

---

**部署完成后，你的AI增强版小说章节拆分工具就可以在互联网上安全使用了！** 