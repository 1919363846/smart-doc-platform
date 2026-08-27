# smart-doc-platform

智能文档处理平台 —— A23 外包杯参赛作品。

基于 Spring Boot + 智谱 AI（GLM-4）+ MongoDB 的智能文档处理系统，支持 AI 多轮对话、文件上传解析、按需生成并美化 docx / xlsx 文档。

## 技术栈

- **后端**：Spring Boot 3.0.2 · Java 17 · MongoDB · Apache POI · springdoc-openapi
- **前端**：Vue 3 · vue-router · axios · Vue CLI 5
- **AI**：智谱 AI GLM-4（密钥通过环境变量 `ZHIPU_API_KEY` 注入，不入库）
- **脚本**：Python（AI 回复与生成文档的格式美化）

## 功能

- 用户登录 / 注册
- 与 AI 多轮对话，上下文关联，可注入上传文件内容
- 文件上传与云仓库管理
- AI 生成 docx / xlsx 文档，自动格式美化
- 暂存区临时文件管理

## 目录结构

```
back/    Spring Boot 后端（controller / service / repository / model / util）
front/   Vue 3 前端（components/work-manager 对话区与各模态框）
```

## 快速开始

```bash
# 1. 启动 MongoDB（默认 localhost:27017）

# 2. 后端
cd back
$env:ZHIPU_API_KEY="你的智谱AI Key"   # Windows PowerShell
mvn spring-boot:run

# 3. 前端
cd front
npm install
npm run serve
```

后端默认端口 `8081`，前端由 `vue-cli-service serve` 提供。


