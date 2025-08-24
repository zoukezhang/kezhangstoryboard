# 分镜故事板项目

![Version](https://img.shields.io/badge/version-v1.0.0-blue.svg)
![Status](https://img.shields.io/badge/status-stable-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

## 版本信息

**当前版本**: v1.0.0  
**发布日期**: 2025年8月24日  
**版本状态**: 稳定版本  

### 版本历史

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

> 🎆 **v1.0.0 首个正式版本已发布！** 支持完整的分镜编辑流程，从项目创建到PDF导出、分享发布一站式解决方案。

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

### 导出和分享
- [x] PDF导出
- [x] 分镜预览
- [x] 分享链接生成
- [x] 临时访问控制

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
│   ├── uploads/           # 上传文件存储
│   ├── database.sqlite    # SQLite数据库文件
│   └── package.json       # 依赖配置
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

```bash
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

```bash
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

**分镜故事板 v1.0.0** - 专业的分镜创作平台  
© 2025 科长分镜故事板 | 首个正式版本发布
