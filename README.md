# 🌟 蓝奏云直链解析工具

一个基于 Cloudflare Worker 的蓝奏云直链解析工具，可以一键获取蓝奏云分享链接的真实下载地址，跳过所有中间页面和广告。

## ✨ 功能特点

- 🚀 **一键解析**：自动解析蓝奏云分享链接
- ⚡ **直接下载**：重定向到真实文件下载地址
- 🔍 **调试模式**：支持详细解析过程查看
- 🌐 **跨平台**：在任何设备浏览器中均可使用
- 🆓 **完全免费**：基于 Cloudflare Worker 免费额度
- 🔒 **隐私安全**：不存储任何用户数据

## 🚀 快速开始

### 基本用法

**体验地址**
https://lanzou.jasmiam.top

1. **获取蓝奏云分享链接**
例如：https://wwi.lanzoup.com/i12345678

2. **访问解析工具**
https://你的worker.workers.dev/?url=你的蓝奏云链接

3. **自动开始下载**
- 浏览器会自动重定向到真实下载地址

### 示例

直接下载模式

https://lanzou-demo.workers.dev/?url=https://wwi.lanzoup.com/i12345678 

调试查看模式

https://lanzou-demo.workers.dev/?url=https://wwi.lanzoup.com/i12345678&debug=1 

## 🛠️ 部署到 Cloudflare Worker

### 前置要求

- [Cloudflare 账号](https://dash.cloudflare.com/sign-up)
- 自定义域名（可选）
- 基本的计算机操作能力

### 部署步骤

1. **注册 Cloudflare 账号**
   - 访问 [Cloudflare 注册页面](https://dash.cloudflare.com/sign-up)
   - 完成邮箱验证

2. **创建 Worker 服务**
   - 登录 [Cloudflare 仪表板](https://dash.cloudflare.com/)
   - 左侧菜单选择 "Workers"
   - 点击 "Create a Service"

3. **配置服务设置**
   - 服务名称：`lanzou-parser`（或其他名称）
   - 选择 "HTTP handler" 模板
   - 选择免费计划

4. **上传代码**
   - 复制本项目的完整代码
   - 在 Worker 编辑器中粘贴代码
   - 点击 "Save and Deploy"

5. **测试部署**
   - 访问你的 Worker 地址进行测试
   - 格式：`https://你的服务名称.你的账号子域.workers.dev`

## 🔒 隐私与安全

- ❌ 不存储用户文件内容
- ❌ 不记录下载历史  
- ❌ 不收集个人信息
- ✅ 所有处理在内存中完成
- ✅ HTTPS加密传输
- ✅ Cloudflare安全防护

## ❓ 常见问题

### Q1: 为什么需要这个工具？
A: 蓝奏云下载需要多次跳转和等待，这个工具可以跳过广告和等待时间，直接获取真实下载链接。

### Q2: 是否支持所有蓝奏云链接？
A: 支持大部分链接，但需要提取码的私密链接或已失效的链接可能无法解析。

### Q3: 有没有使用限制？
A: Cloudflare Worker免费版有每日10万次请求限制，个人使用完全足够。

### Q4: 如何更新解析逻辑？
A: 直接在Cloudflare Worker编辑器中更新代码并重新部署。

## 📞 技术支持

如果遇到问题：

1. 首先使用 `&debug=1` 参数查看详细错误信息
2. 检查蓝奏云链接是否有效
3. 在GitHub Issues中提交问题

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

---

**⭐ 如果这个项目对你有帮助，请给个Star！**
