# Docusaurus Documentation Project Information

## Project Overview
This is a Docusaurus-based documentation site built to create and maintain technical documentation for the GPT API Proxy service. Docusaurus is a modern static website generator that helps build documentation websites quickly and easily.

## Project Structure
The project follows the standard Docusaurus structure:
- `/docs`: Contains all documentation markdown files
- `/blog`: Contains blog posts
- `/src`: Contains React components and custom pages
- `/static`: Contains static assets like images
- `/i18n`: Contains internationalization files for different languages (currently supports English, Simplified Chinese, and Brazilian Portuguese)

## Key Features
1. **Multi-language Support**: The documentation is available in English, Simplified Chinese (zh-Hans), and Brazilian Portuguese (pt-BR).
2. **Search Functionality**: Integrated search using `@easyops-cn/docusaurus-search-local` plugin with Chinese language support.
3. **Blog Section**: Separate blog area for announcements and updates.
4. **Custom Homepage**: Modified home page that automatically redirects to documentation.
5. **Markdown + MDX Support**: Documentation written in Markdown with MDX for interactive components.

## Configuration
The site is configured through `docusaurus.config.ts` with the following main settings:
- Base URL: `https://docs.llmproai.xyz`
- Default locale: English with additional locales for Chinese and Portuguese
- Theme customization via `src/css/custom.css` (current theme uses light blue colors)
- Navigation structure defined in the themeConfig section

## Development Workflow
Development commands are available in `package.json`:
- `npm start`: Start the development server

## Documentation Structure
The documentation follows a sidebar structure automatically generated from the folder structure in the `/docs` directory, with the main entry point being `docs/intro.md`.

## Media and Assets
Static assets are stored in the `/static` directory, with configuration in `.gitten/config.json` specifying `static` as the media folder.

## Current Status
The documentation is in active development with several example pages and translations already in place. The content about the GPT API Proxy service is being expanded, particularly in the "API Docs" section.

## 编辑须知 (Guidelines for AI Editors)

### Markdown 语法指南 (Markdown Syntax Guidelines)
1. **基本语法** (Basic Syntax):
    markdown 语法

2. **Docusaurus 特殊语法** (Docusaurus-Specific Syntax):
   - 前端元数据 (Front Matter): 
     ```
     ---
     sidebar_position: 1
     title: 页面标题
     description: 页面描述
     ---
     ```
   - Admonitions (提示框):
     ```
     :::tip 提示标题
     提示内容
     :::

     :::warning 警告标题
     警告内容
     :::

     :::danger 危险标题
     危险内容
     :::
     ```
   


4. **MDX 组件** (MDX Components):
   - 可以在 Markdown 中使用 React 组件
   - 组件定义使用标准 JSX 语法
   - 示例:
     ```jsx
     export const Highlight = ({children, color}) => (
       <span style={{backgroundColor: color}}>
         {children}
       </span>
     );

     <Highlight color="#1877F2">高亮文本</Highlight>
     ```

### 多语言支持指南 (Multilingual Guidelines), attention: 只有指定翻译任务时才参考此指南
1. **创建翻译文件**:
   - 新文档应优先创建英文版本
   - 翻译文件位于 `i18n/zh-Hans/` 和 `i18n/pt-BR/` 目录

2. **翻译协作**:
   - 确保专业术语在所有语言中保持一致
   - 保留原文中的代码示例，仅翻译注释
   - 可使用 `npm run write-translations` 生成待翻译文件
3. prompt
You are a professional interpreter who can translate articles from ${chinese} to ${targetLang}.User will provide the original article directly, without any other information.The article is written in plain text, Markdown format or MDX format. You should keep the original Markdown syntax or MDX syntax if there are any. MDX syntax looks like Markdown + HTML. Also, you should not translate meaningful items, such as URLs.Reply with the translated article. Do not include the original article in your reply. Do not include anything other than the translated article in your reply.Do not stop your response until you have finished translating the entire article.




### 图片和资源 (Images and Assets)
1. **图片存放**:
   - 将图片放置在 `/static/img/` 目录下
   - 在 Markdown 中引用: `![描述](/img/图片名.png)`
   
2. **组织结构**:
   - 为特定文档创建子文件夹
   - 使用有意义的文件名

### 文档质量标准 (Documentation Quality Standards)
1. **内容要求**:
   - 文档应清晰、简洁、准确
   - 示例代码必须能够正常运行
   - 技术描述应准确无误
   - 解释复杂概念时提供图表或类比

2. **格式标准**:
   - 一致的标题大小写
   - 一致的代码风格
   - 恰当的段落长度 (避免过长段落)
   - 合理使用列表和表格组织信息

### 编辑限制 (Editing Restrictions)

**不能做的事** (What You Cannot Do):
- 删除现有重要内容
- 添加不准确的技术信息
- 添加与项目无关的内容
- 生成与文档主题无关的营销内容
- 更改已建立的术语一致性