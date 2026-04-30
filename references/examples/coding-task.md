# 编程任务示例

## 原始指令

```
帮我写一个用户登录功能
```

## 分析结果

| 要素 | 状态 | 诊断 |
|------|------|------|
| 角色 | 缺失 | AI不知道是写前端还是后端 |
| 任务 | 模糊 | "登录功能"范围不明确（验证？加密？session？） |
| 背景 | 缺失 | 不知道技术栈、安全要求 |
| 格式 | 缺失 | 不知道输出代码还是文档 |

## 优化后提示词

```markdown
## 角色
你是一位5年经验的Java后端开发工程师，熟悉Spring Boot安全架构。

## 任务
实现一个用户登录API接口，包含：
1. 用户名/密码验证
2. JWT token生成
3. 登录失败次数限制（3次锁定）
4. 登录日志记录

## 输入/背景
- 技术栈：Spring Boot 2.7 + Spring Security + JWT
- 数据库：MySQL，用户表已存在（字段：id, username, password_hash, status）
- 安全要求：密码使用BCrypt加密，token有效期24小时
- 参考文档：项目中已有AuthController.java，需要扩展

## 输出格式
输出完整的代码文件，包含：
1. LoginController.java（控制器层）
2. LoginService.java（服务层）
3. LoginRequest.java（请求DTO）
4. LoginResponse.java（响应DTO）

## 修改说明表格

| 文件 | 主要功能 | 关键方法 |
|------|----------|----------|
| LoginController | 接收登录请求 | login() |
| LoginService | 验证逻辑 | authenticate() |
| LoginRequest | 请求数据封装 | username, password |
| LoginResponse | 响应数据封装 | token, expireTime |

## 约束
- 遵循现有项目的包结构
- 增加必要的安全注释
- 不修改现有AuthController的核心逻辑
```

## 优化要点

1. **补充角色**：明确了"Java后端开发工程师"角色，定义能力边界
2. **量化任务**：将"登录功能"拆解为4个具体子功能
3. **增加背景**：提供技术栈、数据库结构、安全要求等决策依据
4. **明确格式**：规定输出4个代码文件 + 修改说明表格
5. **消除歧义**：明确"登录功能"包含验证、token、锁定、日志等具体内容