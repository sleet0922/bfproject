# 聊天应用后端

这是基于Golang的即时聊天应用后端，提供API接口和WebSocket服务。

功能
- [ x ] 用户认证系统，注册、登录
- [ x ] MySQL存储聊天消息、用户、好友关系和群组信息

好友：
- [ x ] 添加好友
- [ x ] 发送消息给好友

群组：
- [ x ] 添加群组
- [ x ] 邀请好友加入群组
- [ x ] 在群组里发送消息

# 聊天应用后端
## 技术栈

- Golang
- Gin框架
- Gorm
- MySQL
- WebSocket
## 开发指南

```bash
go mod tidy
go run main.go
```

## 总结

我已经完成了将数据库从MongoDB改为MySQL的所有必要修改：

### 主要修改内容：

1. **配置文件**：移除了MongoDB配置，添加了完整的MySQL配置，使用你提供的连接信息（117.72.38.183，用户名root，密码zyz20050922）

2. **数据库初始化**：完全重写了数据库连接逻辑，使用GORM连接MySQL

3. **数据模型**：将所有模型从MongoDB的BSON格式改为GORM的MySQL格式

4. **依赖项**：更新了go.mod文件，添加了GORM和MySQL驱动依赖

5. **文档**：更新了README文件，移除MongoDB相关说明

### 下一步操作：

1. 运行以下命令安装新的依赖：
```bash
cd backend
go mod tidy
```

2. 确保你的MySQL服务器（117.72.38.183）已经启动，并且数据库`gin_vue_chat`已经创建

3. 启动应用：
```bash
go run main.go
```

应用启动时会自动创建所有必要的数据库表结构。现在你的聊天应用已经完全使用MySQL作为数据库了。