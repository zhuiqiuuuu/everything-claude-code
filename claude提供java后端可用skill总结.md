# Java后端SpringBoot开发可用Skill总结

基于ECC项目技能库分析，整理出适用于Java后端SpringBoot开发的核心技能清单。

## 🎯 核心SpringBoot技能

### 1. springboot-patterns - SpringBoot架构模式
- **描述**: Spring Boot架构和API模式，用于构建可扩展的生产级服务
- **核心内容**: 
  - REST API结构与控制器设计
  - Repository模式(Spring Data JPA)
  - 服务层与事务管理
  - DTO验证与异常处理
  - 缓存、异步处理、日志记录
  - 中间件/过滤器、速率限制、后台任务
- **使用场景**: 构建REST API、设计分层架构、配置数据访问、添加验证和异常处理

### 2. springboot-tdd - 测试驱动开发
- **描述**: Spring Boot的TDD工作流，确保80%+测试覆盖率
- **核心内容**:
  - JUnit 5 + Mockito单元测试
  - MockMvc Web层测试
  - SpringBootTest集成测试
  - Testcontainers容器化测试
  - JaCoCo覆盖率统计
  - 测试数据构建器模式
- **使用场景**: 新功能开发、Bug修复、代码重构、确保代码质量

### 3. springboot-security - SpringBoot安全最佳实践
- **描述**: Spring Security认证授权、输入验证、CSRF、CORS、密钥管理等
- **核心内容**:
  - JWT认证过滤器和令牌验证
  - 方法级授权(@PreAuthorize)
  - Bean Validation输入验证
  - SQL注入防护
  - 密码编码(BCrypt/Argon2)
  - CSRF配置、CORS策略
  - 密钥管理、安全头部配置
  - 速率限制、依赖安全扫描
- **使用场景**: 添加认证授权、处理用户输入、创建API端点、管理密钥

### 4. springboot-verification - SpringBoot验证循环
- **描述**: 发布前的完整验证流程：构建→静态分析→测试→安全扫描
- **核心内容**:
  - Maven/Gradle构建验证
  - SpotBugs、PMD、Checkstyle静态分析
  - 单元测试、集成测试、API测试
  - JaCoCo覆盖率验证(80%+)
  - OWASP依赖安全检查
  - 代码差异审查
  - 持续验证模式
- **使用场景**: PR前验证、重大重构后、预部署检查、CI/CD流水线

## 🔧 Java专项技能

### 5. java-coding-standards - Java编码标准
- **描述**: Java 17+编码规范，注重可读性和可维护性
- **核心内容**:
  - 命名规范(PascalCase、camelCase、UPPER_SNAKE_CASE)
  - 不可变性与记录类使用
  - Optional最佳实践
  - Stream API使用规范
  - 异常处理策略
  - 泛型与类型安全
  - 项目结构布局
  - 代码异味避免
  - 日志规范(SLF4J)
- **使用场景**: Java代码编写、代码审查、规范化项目结构

### 6. jpa-patterns - JPA/Hibernate模式
- **描述**: JPA实体设计、关系映射、查询优化和性能调优
- **核心内容**:
  - 实体设计与表映射
  - 关系配置与N+1查询预防
  - Repository模式与自定义查询
  - 事务管理与只读优化
  - 分页与排序实现
  - 索引策略与性能优化
  - HikariCP连接池配置
  - 二级缓存策略
  - 迁移工具集成(Flyway/Liquibase)
- **使用场景**: 数据建模、JPA配置、查询优化、性能调优

## 🏗️ 通用后端技能

### 7. backend-patterns - 后端架构模式
- **描述**: 通用后端架构模式和最佳实践
- **核心内容**:
  - RESTful API设计原则
  - 仓库模式与服务层模式
  - 中间件模式(认证、日志、速率限制)
  - 数据库查询优化与N+1预防
  - 事务模式与错误处理
  - 缓存策略(Redis、内存缓存)
  - 重试机制与指数退避
  - JWT认证与RBAC授权
  - 速率限制实现
  - 结构化日志与监控
- **使用场景**: 通用后端架构设计、API开发、性能优化

### 8. api-design - API设计模式
- **描述**: REST API设计规范，包含资源命名、状态码、分页、错误处理等
- **核心内容**:
  - RESTful URL结构与命名规范
  - HTTP方法与状态码语义
  - 统一响应格式与错误响应
  - 分页策略(偏移量vs游标)
  - 过滤、排序与搜索
  - 稀疏字段集与字段选择
  - 认证授权模式
  - 速率限制与版本控制
  - OpenAPI规范与文档
- **使用场景**: 设计新API、审查现有API、构建公共API

## 🗄️ 数据与部署技能

### 9. database-migrations - 数据库迁移
- **描述**: 安全的数据库模式变更和数据迁移最佳实践
- **核心内容**:
  - 迁移安全原则与检查清单
  - PostgreSQL安全迁移模式
  - Prisma、Drizzle、Django、golang-migrate工作流
  - 零停机迁移策略(扩展-收缩模式)
  - 大数据批量迁移
  - 并发索引创建
  - 迁移反模式避免
- **使用场景**: 表结构变更、生产环境部署、数据迁移

### 10. postgres-patterns - PostgreSQL模式
- **描述**: PostgreSQL查询优化、索引设计和性能调优
- **核心内容**:
  - 索引类型选择与应用场景
  - 数据类型最佳实践
  - 复合索引与覆盖索引设计
  - 部分索引与RLS策略优化
  - UPSERT与游标分页
  - 队列处理模式
  - 反模式检测与性能监控
  - 配置模板与优化建议
- **使用场景**: PostgreSQL数据库开发、查询优化、性能调优

### 11. docker-patterns - Docker模式
- **描述**: Docker和Docker Compose容器化开发最佳实践
- **核心内容**:
  - Docker Compose本地开发栈配置
  - 多阶段Dockerfile优化
  - 服务发现与网络配置
  - 卷策略与数据持久化
  - 容器安全最佳实践
  - 调试工具与命令
  - 安全反模式避免
- **使用场景**: 本地开发环境搭建、容器化部署、多服务编排

## 💡 技能组合使用建议

### 新项目启动阶段
```
springboot-patterns + java-coding-standards + jpa-patterns + api-design
```
- 建立标准架构模式
- 遵循Java编码规范  
- 设计数据访问层
- 制定API设计规范

### 功能开发阶段
```
springboot-tdd + springboot-security + database-migrations + backend-patterns
```
- 测试驱动开发确保质量
- 安全实现贯穿全程
- 数据库变更管理
- 通用后端模式应用

### 测试验证阶段
```
springboot-verification + springboot-tdd + postgres-patterns
```
- 完整验证循环
- 测试覆盖率保证
- 数据库性能优化

### 部署发布阶段
```
springboot-verification + docker-patterns + postgres-patterns
```
- 发布前全面验证
- 容器化部署
- 数据库优化配置

## 📝 使用最佳实践

### ✅ 推荐做法
- **优先使用核心SpringBoot技能**建立标准架构
- **结合TDD技能**确保代码质量和测试覆盖率
- **安全技能贯穿全程**，不要事后补救
- **验证技能强制执行**，确保发布前质量

### ❌ 避免做法  
- 忽视安全技能，安全应贯穿开发全程
- 跳过测试验证步骤
- 在生产环境手动修改数据库结构
- 忽视代码规范和架构模式

这套技能体系完整覆盖了Java后端SpringBoot开发的整个生命周期，为开发团队提供了从项目初始化到部署验证的全方位技能支持。