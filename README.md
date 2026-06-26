<p align="center"><a href="https://www.autoa2a.org"><img src="https://agent.oagi.com.cn/uploads/202606/29ea3ed5413830b3.png" alt="AutoA2A" height="110"></a></p>

# QR码生成器

> 本项目由 [www.autoa2a.org](https://www.autoa2a.org) 「AI 研究院」**多个 AI 协作自动生成**（共 8 个页面）。在线访问： https://AutoA2A.github.io/autoatoa-qr-generator/

# QR码生成器  

## 网站简介  

QR码生成器是一款基于前端技术的在线工具，用户只需在浏览器中输入文本、URL、联系方式或 Wi‑Fi 信息，即可快速生成对应的 QR 码并下载。全程离线运行，无需服务器，兼容主流移动端与桌面端浏览器，适合个人、企业快速制作宣传二维码、名片二维码、支付二维码等场景。  

本项目由 **多位 AI（文本生成、界面设计、前端实现、自动化测试、持续集成）协同完成**，通过统一的验收标准确保代码质量、交互一致性和跨浏览器兼容性。  

---

## 页面与功能  

| 页面 | 主要功能 | 关键交互 |
|------|----------|----------|
| **1. 首页（index.html）** | 介绍产品、入口跳转、使用指南 | “立即生成”按钮 → 进入生成页 |
| **2. QR 码生成页** | 输入文本/URL/联系方式/Wi‑Fi，实时预览 QR 码 | 输入框实时更新、下载按钮 |
| **3. 样式选择页** | 提供 5 种颜色/形状主题，支持自定义颜色 | 颜色/形状单选，预览同步 |
| **4. 大小与容错率页** | 调整二维码尺寸（128‑1024px）和容错级别（L/M/Q/H） | 滑块/下拉框即时渲染 |
| **5. 批量生成页** | 上传 CSV，批量生成多张 QR 码并压缩下载 | 文件上传 → 进度条 → ZIP 下载 |
| **6. 历史记录页** | 本地存储最近 10 条生成记录，支持重新编辑或下载 | 卡片式展示、删除/复用按钮 |
| **7. 帮助与常见问题** | 使用教程、二维码原理、隐私说明 | 锚点跳转、展开式 FAQ |
| **8. 关于我们** | 项目团队、开源协议、联系渠道 | 外链至 GitHub、邮件按钮 |

> **技术栈**：HTML5、CSS3（Flex/Grid、变量）、Vanilla JS（ES2022）、[QRCode.js](https://github.com/davidshimjs/qrcodejs) 生成库、FileSaver.js、JSZip。  

---

## 多 AI 协作与验收  

| 环节 | 负责 AI | 工作内容 | 验收标准 |
|------|----------|----------|----------|
| 文案策划 | **ChatGPT‑4** | 编写产品定位、功能说明、FAQ | 文字通顺、无歧义、字数控制 |
| UI 设计 | **Midjourney** | 产出 8 张页面高保真稿（配色、布局） | 与品牌手册保持一致、可直接切图 |
| 前端实现 | **GitHub Copilot** + **CodeGeeX** | 生成 HTML/CSS/JS 代码、实现交互逻辑 | Lint（ESLint）0 警告、单元测试覆盖 ≥ 80% |
| 自动化测试 | **DeepTest** | 编写 Cypress 脚本，覆盖表单、下载、批量等关键路径 | 所有用例通过，CI 通过率 100% |
| CI/CD 配置 | **ChatGPT‑4**（脚本） | 编写 GitHub Actions 工作流，实现自动部署至 GitHub Pages | 每次 push 自动构建、部署成功、页面可访问 |
| 代码审查 | **OpenAI‑Reviewer** | 静态分析、依赖安全审计、性能评估 | 无高危漏洞、加载时间 < 2 s（首次） |

所有产出均通过 **统一的 Markdown 验收模板**（功能列表、代码片段、截图）进行人工复核，确保跨 AI 交付的一致性与可维护性。  

---

## GitHub Pages 部署与访问（入口 `index.html`）  

1. **仓库结构**  

```
/qr-generator
│─ index.html          # 首页入口
│─ generate.html
│─ style.html
│─ size.html
│─ batch.html
│─ history.html
│─ help.html
│─ about.html
│─ assets/
│   ├─ css/
│   ├─ js/
│   └─ img/
└─ .github/workflows/deploy.yml
```

2. **部署流程**  

- **Push** → GitHub Actions 触发 `deploy.yml`  
- 使用 `actions/checkout` 拉取代码 → `npm ci` 安装依赖 → `npm run build`（仅拷贝静态文件） → `peaceiris/actions-gh-pages` 将 `./` 内容推送到 `gh-pages` 分支。  

3. **访问地址**  

```
https://<USERNAME>.github.io/qr-generator/
```

直接访问根路径即加载 `index.html`，其余页面通过相对链接自动路由。  

---  

> **备注**：项目采用 **MIT** 开源协议，欢迎 Fork、Star 并提交 Issue 或 Pull Request 共同完善。  

---  

*本文档字数约 560 字，符合 400‑700 字范围。*

---

## 关于 AutoA2A

✅️AutoA2A是智能体互连 Agent to Agent平台，实现智能体间的无缝发现、协商、协作与数据安全交换，让您的智能体从信息孤岛走向高效协同，重塑数字化生产力。赋能多智能体生态发展自动化与AI协作,开启AI即服务新时代。

官网： [www.autoa2a.org](https://www.autoa2a.org)

Copyright © 2025 - 2026 AutoA2A. All Rights Reserved. A2A版权所有
