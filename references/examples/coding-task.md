# 编程任务示例

## 任务目标
实现用户登录API接口（含验证、JWT、锁定、日志）

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

## 输出格式
1. LoginController.java（控制器层）
2. LoginService.java（服务层）
3. LoginRequest.java（请求DTO）
4. LoginResponse.java（响应DTO）

## 约束
- 遵循现有项目的包结构
- 不修改现有AuthController的核心逻辑
```

## 注意事项
- 原指令"登录功能"模糊，追问后拆解为4个子功能
- 角色=工程师（从"功能"关键词推断）
- 格式=代码文件（从编程任务推断）

## 后续任务建议
- 提供现有AuthController.java代码片段，确保风格一致
- 确认用户表字段是否需要扩展（如lock_count）