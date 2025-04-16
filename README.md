# MentorSelectGuide_WHUCS

这是一个基于 Vue 3 和 Spring Boot 开发的武汉大学计算机学院导师指南系统，旨在为学生科研之路提供智能化指南。

## 项目特点

- 基于 DeepSeek API 的智能推荐系统
- 实时流式对话响应（SSE）
- 前后端分离架构
- RESTful API 设计
- 标签化导师筛选
- 智能化导师匹配算法

## 技术栈

### 前端
- **核心框架**: Vue 3
- **UI组件库**: Element Plus
- **路由管理**: Vue Router 4
- **HTTP客户端**: Fetch API
- **图标库**: Element Plus Icons
- **Markdown渲染**: Marked
- **开发工具**: Vue CLI

### 后端
- **核心框架**: Spring Boot
- **AI集成**: DeepSeek Chat API
- **数据库**: MySQL
- **HTTP客户端**: Apache HttpClient
- **JSON处理**: Jackson
- **构建工具**: Maven
- **服务器推送**: SSE (Server-Sent Events)

## 系统功能

### 已实现功能
- AI 智能对话（基于 SSE 流式响应）
- 智能导师推荐
  - 基于标签的导师筛选
  - 个性化推荐算法
  - 实时对话反馈
- 基础页面框架
- 导师信息展示
- 标签化筛选系统

### 待实现功能
- 科研方向信息查询系统
- 教师评价系统
- 用户认证系统
- 个人中心

## 项目结构

```
MentorSelectGuide_WHUCS/
├── UI_vue/                  # 前端项目
│   └── ui/
│       ├── public/          # 静态资源
│       ├── src/
│       │   ├── assets/      # 资源文件
│       │   ├── components/  # 通用组件
│       │   │   ├── Header/  # 头部组件
│       │   │   └── Footer/  # 底部组件
│       │   ├── router/      # 路由配置
│       │   ├── views/       # 页面组件
│       │   │   ├── Home/    # 首页
│       │   │   ├── AIRecommend/  # AI推荐页
│       │   │   └── About/   # 关于页面
│       │   ├── App.vue      
│       │   └── main.js      
│       └── package.json     
│
└── src/                     # 后端项目
    ├── main/
    │   ├── java/
    │   │   └── com/example/whucs_mentorguide/
    │   │       ├── controller/    # 控制器
    │   │       │   └── OpenAIController.java  # AI对话控制器
    │   │       ├── service/       # 服务层
    │   │       ├── model/         # 数据模型
    │   │       └── config/        # 配置类
    │   └── resources/
    │       ├── application.properties  # 应用配置
    │       └── templates/         # 模板文件
    └── test/                # 测试目录
```

## 快速开始

### 环境要求
- Node.js >= 14.0.0
- Java >= 17
- Maven >= 3.6
- MySQL >= 8.0

### 前端启动
```bash
cd UI_vue/ui
npm install
npm run serve
```

### 后端启动
```bash
# 使用Maven启动Spring Boot应用
./mvnw spring-boot:run
```

## 配置说明

### DeepSeek API配置
在 `application.properties` 中配置：
```properties
ai.config.deepseek.apiKey=your_api_key
ai.config.deepseek.baseUrl=https://api.deepseek.com/v1
```

### 数据库配置
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/mentor_guide
spring.datasource.username=<username>
spring.datasource.password=<password>
```

## 开发指南

### 前端开发
1. 组件开发遵循 Vue 3 组合式 API
2. 使用 Element Plus 组件库
3. 使用 ESLint 进行代码规范检查
4. 实现响应式设计

### 后端开发
1. 遵循 RESTful API 设计规范
2. 使用统一的响应格式
3. 实现完整的错误处理
4. 添加详细的日志记录

## 部署说明

### 前端部署
```bash
npm run build
```
将 `dist` 目录下的文件部署到 Web 服务器

### 后端部署
```bash
mvn clean package
java -jar target/whucs-mentorguide.jar
```

## 浏览器兼容性

- Chrome (推荐，最新版本)
- Firefox (最新版本)
- Edge (最新版本)
- Safari (最新版本)

## 开发计划

### 近期计划
1. 优化 AI 推荐算法
2. 完善错误处理机制
3. 添加用户反馈功能
4. 优化页面响应速度
5. 实现数据缓存机制

### 长期计划
1. 开发移动端应用
2. 添加数据分析功能
3. 实现智能化教学资源推荐
4. 建立导师评价体系
5. 开发管理员后台系统

## 贡献指南

1. Fork 项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 提交 Pull Request

## 许可证

本项目采用 MIT 许可证
