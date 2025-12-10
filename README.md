# Gin-Vue-Chat 即时聊天应用
## 技术栈
### 后端
- Golang
- Gin框架
- Gorm
- MySQL
- WebSocket

## 项目结构

```
Gin-Vue-Chat/
├── frontend/           # 前端Vue项目
└── backend/            # 后端Golang项目
```

该应用已经实现了所有基本功能：
- 用户注册和登录
- 添加好友和私聊
- 创建群组和群聊
- 实时消息推送

## 开发指南

### 前端开发

```bash
cd frontend
pnpm install
pnpm run dev
```

### 后端开发

```bash
cd backend
go mod tidy
go run main.go
```

## 部署指南

待补充