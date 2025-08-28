# 分镜故事板项目

![Version](https://img.shields.io/badge/version-v1.0.3-blue.svg)
![Status](https://img.shields.io/badge/status-testing-yellow.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

## 版本信息

**当前版本**: v1.0.3  
**发布日期**: 2025年8月28日  
**版本状态**: 测试版本  

### 版本历史

#### v1.0.3 (2025-08-28) - 稳定性优化版
- ✅ **批量上传优化**: 修复批量上传图片后分镜列表需要手动刷新才能显示新图片的问题
- ✅ **自动刷新**: 批量上传完成后自动刷新分镜列表，确保新图片立即显示
- ✅ **代码清理**: 删除不必要的测试文件和SQL相关文件，保持项目整洁
- ✅ **依赖优化**: 移除项目中不再使用的SQLite依赖（better-sqlite3和sqlite3）
- ✅ **文档整理**: 删除过时的.md文档，保留核心必要文件

**重点改进**:
- 批量上传图片后无需手动刷新页面，提升用户体验
- 项目结构更加简洁，移除不必要的文件和依赖
- 文档更加精简，只保留核心必要文件

#### v1.0.2 (2025-08-25) - 幻灯片缩略图体验优化版
- ✨ **幻灯片缩略图优化**: 缩略图从页面底部移动到图片区域底部悬浮显示
- 🎨 **视觉体验提升**: 半透明黑色背景 + 毛玻璃效果，现代化设计
- 📱 **响应式设计**: 缩略图在不同屏幕尺寸下智能调整大小
- 🚫 **幻灯片模式优化**: 移除底部操作栏，避免遮挡缩略图显示
- ⚡ **性能优化**: 缩略图不再占用额外页面空间，提升主内容区域显示
- 🎯 **交互优化**: 缩略图悬停放大效果，更明显的选中高亮
- 🖱️ **列表视图增强**: 缩略图悬停显示操作按钮，支持图片替换和删除
- 🛡️ **安全确认**: 列表视图删除图片提供确认对话框，防止误操作

**重点改进**:
- 缩略图悬浮显示在图片区域底部，不再被页面底部操作栏遮挡
- 类似PowerPoint的缩略图体验，更加直观和专业
- 智能宽度控制，缩略图不超出图片区域范围
- 列表视图缩略图交互增强，提供了更便捷的图片管理方式

#### v1.0.1 (2025-08-25) - 中文字体优化版
- ✨ **PDF中文字体支持**: 集成中文字体文件到项目中，无需依赖系统字体
- 📝 **项目内置字体**: 添加 Hiragino Sans GB.ttc、Arial Unicode.ttf 和 Arial.ttf
- 🔧 **智能字体回退**: 多级字体加载机制，确保跨平台兼容性
- 📊 **中文内容优化**: 改进中文文本处理和显示效果
- 📁 **部署文档**: 新增 FONT_DEPLOYMENT.md 和字体使用说明
- 🚀 **部署优化**: 简化部署流程，提高不同环境的兼容性
- 🔒 **用户体验改进**: 优化登录错误提示，区分未注册和密码错误

**重点改进**:
- PDF导出现在完全支持中文显示，无需依赖系统字体
- 提供完整的字体部署方案和文档
- 增强用户登录体验，提供更友好的错误提示

#### v1.0.0 (2025-08-24) - 首个正式版本
- ✅ 完整的用户认证系统 (注册、登录、密码修改)
- ✅ 项目管理功能 (创建、编辑、删除项目)
- ✅ 分镜编辑器 (添加、删除、排序分镜)
- ✅ 自定义字段配置 (11个可选字段)
- ✅ 图片上传和管理
- ✅ 实时自动保存
- ✅ 拖拽排序功能
- ✅ PDF导出功能
- ✅ 分享链接生成
- ✅ 响应式设计
- ✅ 前后端分离架构
- ✅ SQLite数据库支持
- ✅ 端口配置优化
- ✅ 图片代理功能

**技术亮点**:
- Vue 3 + Vite 6.0 现代前端技术栈
- Node.js + Express.js 后端架构
- JWT身份认证
- Element Plus UI组件库
- Pinia状态管理
- 支持Docker部署

---

一个专业的分镜头脚本编辑平台，支持分镜创建、编辑、预览和分享功能。

> 🎆 **v1.0.3 稳定性优化版已发布！** 修复了批量上传图片后需要手动刷新的问题，同时进行了代码清理和优化，使项目更加稳定和简洁。

## 项目概述

分镜故事板是一个前后端分离的Web应用程序，帮助用户创建和管理分镜头脚本。该平台提供直观的用户界面，支持拖拽排序、实时保存、图片上传等功能。

## 技术栈

### 前端
- Vue 3.5+ (Composition API)
- Vite 6.0+ (构建工具)
- Element Plus (UI组件库)
- Pinia (状态管理)
- Vue Router 4 (路由管理)
- Axios (HTTP客户端)
- Vue Draggable Next (拖拽功能)

### 后端
- Node.js 18+
- Express.js (Web框架)
- SQLite (数据库，可轻松切换至MySQL)
- JWT (身份认证)
- BCrypt (密码加密)
- Multer (文件上传)
- PDFKit (PDF导出)

## 🆕 中文字体支持

### 字体集成
项目已内置中文字体文件，无需依赖系统字体：

- **Noto Sans CJK SC Regular** - Google开源中文字体（首选，完美支持）
- **Arial.ttf** - 基础英文字体（备选）

### 技术优势
- ✅ **PDFKit完全兼容**: 使用OTF格式字体，确保PDF导出稳定性
- ✅ **开源免费**: Noto Sans CJK无商业使用限制
- ✅ **体积优化**: 单一字体文件(16MB)，相比多字体方案减少体积
- ✅ **中文显示完美**: 支持简体中文、繁体中文全字符集

### 智能加载机制
系统会自动按优先级尝试加载字体，确保在不同平台上都能正确显示中文内容：
1. **Noto Sans CJK SC Regular** - 最佳中文显示效果
2. **Arial.ttf** - 英文字体备选
3. **Helvetica** (内置) - 最终备选方案

### 部署优势
- ✅ **环境独立**: 不依赖系统字体，任何电脑都能正常运行
- ✅ **一键部署**: 字体文件随项目一起打包部署
- ✅ **多平台支持**: Windows、Linux、macOS 全平台兼容
- ✅ **PDF中文完美**: 解决跨平台PDF中文显示问题

📄 **详细文档**: 查看 [FONT_DEPLOYMENT.md](FONT_DEPLOYMENT.md) 了解完整的字体部署指南

## 功能特性

### 用户系统
- [x] 用户注册/登录
- [x] JWT身份认证
- [x] 用户信息管理
- [x] 安全退出

### 项目管理
- [x] 创建新项目
- [x] 项目列表展示
- [x] 编辑项目名称
- [x] 删除项目
- [x] 项目统计信息

### 分镜编辑
- [x] 添加/删除分镜
- [x] 批量添加分镜
- [x] 拖拽排序
- [x] 实时保存
- [x] 图片上传
- [x] 分镜标签和描述编辑
- [x] 三种视图模式：卡片、列表、幻灯片
- [x] 🆕 **幻灯片缩略图优化**: 悬浮显示，类PPT体验
- [x] 🆕 **智能布局**: 缩略图不超出图片区域范围
- [x] 🆕 **列表视图交互**: 缩略图悬停显示操作按钮，支持图片替换和删除

### 导出和分享
- [x] PDF导出 (🆕 中文显示完美支持)
- [x] 分镜预览
- [x] 分享链接生成
- [x] 临时访问控制
- [x] 跨平台部署支持 (🆕 内置开源字体)
- [x] 🆕 **优化界面体验**: 幻灯片模式下隐藏底部操作栏

## 项目结构

```
分镜工具开发/
├── frontend/               # 前端Vue项目
│   ├── src/
│   │   ├── components/     # 可复用组件
│   │   ├── views/         # 页面组件
│   │   ├── stores/        # Pinia状态管理
│   │   ├── router/        # 路由配置
│   │   ├── utils/         # 工具函数
│   │   └── assets/        # 静态资源
│   ├── public/            # 公共资源
│   └── package.json       # 依赖配置
├── backend/               # 后端Node.js项目
│   ├── src/
│   │   ├── routes/        # API路由
│   │   ├── models/        # 数据模型
│   │   ├── middleware/    # 中间件
│   │   ├── config/        # 配置文件
│   │   └── utils/         # 工具函数
│   ├── fonts/             # 🆕 PDF中文字体支持（完美修复）
│   ├── uploads/           # 上传文件存储
│   ├── database.sqlite    # SQLite数据库文件
│   └── package.json       # 依赖配置
├── FONT_DEPLOYMENT.md     # 🆕 字体部署指南
├── THUMBNAIL_HOVER_FEATURE.md # 🆕 缩略图悬停功能说明
└── README.md              # 项目说明
```

## 安装和运行

### 前置要求
- Node.js 18.0+
- npm 8.0+

### 安装依赖

```bash
# 安装后端依赖
cd backend
npm install

# 安装前端依赖
cd ../frontend
npm install
```

### 环境配置

在后端目录创建 `.env` 文件：

```env
NODE_ENV=development
PORT=3002
JWT_SECRET=your-super-secret-jwt-key
CORS_ORIGIN=http://localhost:3000
```

### 启动项目

```bash
# 启动后端服务器 (端口3002)
cd backend
npm start

# 启动前端开发服务器 (端口3000)
cd frontend
npm run dev
```

访问 http://localhost:3000 开始使用应用。

## API文档

### 用户认证
- `POST /api/user/register` - 用户注册
- `POST /api/user/login` - 用户登录
- `GET /api/user/info` - 获取用户信息
- `POST /api/user/logout` - 用户退出

### 项目管理
- `GET /api/project/list` - 获取项目列表
- `POST /api/project/create` - 创建项目
- `GET /api/project/:id` - 获取单个项目
- `PUT /api/project/update/:id` - 更新项目
- `DELETE /api/project/delete/:id` - 删除项目

### 分镜管理
- `GET /api/shot/list/:projectId` - 获取分镜列表
- `POST /api/shot/add` - 添加分镜
- `PUT /api/shot/edit/:id` - 编辑分镜
- `DELETE /api/shot/delete/:id` - 删除分镜
- `PUT /api/shot/sort` - 分镜排序
- `POST /api/shot/upload-image` - 上传图片

### 导出和分享
- `GET /api/export/:projectId` - 导出PDF
- `POST /api/share/create/:projectId` - 创建分享链接
- `GET /api/share/:token` - 访问分享内容

## 数据库设计

### users 表
- id (主键)
- username (用户名)
- email (邮箱)
- password (密码哈希)
- register_time (注册时间)

### projects 表
- id (主键)
- user_id (用户ID，外键)
- name (项目名称)
- shot_count (镜头数量)
- create_time (创建时间)
- last_edit_time (最后编辑时间)

### shots 表
- id (主键)
- project_id (项目ID，外键)
- sort_order (排序)
- tag (标签)
- description (描述)
- image_url (图片URL)
- create_time (创建时间)
- update_time (更新时间)

### shares 表
- id (主键)
- project_id (项目ID，外键)
- token (分享令牌)
- expire_time (过期时间)
- created_at (创建时间)

## 开发指南

### 前端开发
- 使用Vue 3 Composition API编写组件
- 使用Pinia进行状态管理
- 遵循Element Plus设计规范
- 确保响应式设计
- 🆕 **幻灯片视图优化**: 悬浯缩略图设计，避免操作栏遮挡
- 🆕 **条件渲染**: 不同视图模式下UI元素差异化显示

### 后端开发
- 使用Express.js构建RESTful API
- 实施适当的错误处理
- 使用JWT进行身份验证
- 确保数据验证和安全性

### 测试
- 后端API测试使用curl或Postman
- 前端功能测试通过浏览器
- 确保跨浏览器兼容性

## 部署指南

### 生产环境配置
1. 更新环境变量
2. 构建前端项目：`npm run build`
3. 配置反向代理（nginx推荐）
4. 使用PM2管理Node.js进程
5. 配置SSL证书

### Docker部署

**快速部署**:

```
# 1. 下载部署包
wget storyboard-docker-v1.0.0.tar.gz

# 2. 解压部署包
tar -xzf storyboard-docker-v1.0.0.tar.gz
cd storyboard-docker-v1.0.0

# 3. 运行部署脚本
./deploy.sh

# 4. 访问应用
# 前端: http://localhost
# 后端: http://localhost:3002
```

**手动部署**:

```
# 启动服务
docker-compose up -d

# 查看状态
docker-compose ps

# 查看日志
docker-compose logs -f

# 停止服务
docker-compose down
```

**配置说明**: 详细部署文档请查看 `DOCKER_DEPLOY.md`

## 贡献指南

1. Fork项目
2. 创建功能分支
3. 提交更改
4. 推送到分支
5. 创建Pull Request

## 测试账号

邮箱：test@example.com
密码：123456

## 许可证

本项目采用MIT许可证。详细信息请查看LICENSE文件。

## 联系方式

如有问题或建议，请通过以下方式联系：
- 邮箱: 5349589@qq.com
- 项目主页: http://www.seo028.net/storyboard

---

**分镜故事板 v1.0.2** - 专业的分镜创作平台  
© 2025 科长分镜故事板 | 幻灯片缩略图优化版
