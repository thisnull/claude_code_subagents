# Project Prompt Scenarios

简化的项目场景配置文件，用于 `/enhance-prompt` 命令自动添加工作流要求。

## Feature Development - 新功能开发
**Triggers**: implement, add, create, build, develop, new, feature, 实现, 添加, 创建, 构建, 开发, 新功能
**Requirements**:
- 开发前更新需求文档和设计文档
- 实现过程中遵循项目编码规范
- 开发完成后编写单元测试和集成测试
- 更新API文档（如涉及接口变更）

## Bug Fixing - 问题修复
**Triggers**: fix, bug, issue, problem, error, debug, 修复, 错误, 问题, 调试
**Requirements**:
- 修改完成后必须进行测试验证
- 将调试过程和解决方案记录到文档
- 检查是否存在类似的潜在问题
- 更新相关测试用例防止回归

## API Changes - API接口变更
**Triggers**: api, endpoint, route, rest, interface, 接口, 端点, 路由
**Requirements**:
- 更新API文档和接口规范
- 考虑API版本控制和向后兼容性
- 进行API集成测试和契约测试
- 通知API消费者关于变更

## Database Changes - 数据库变更
**Triggers**: database, schema, migration, table, column, 数据库, 表结构, 迁移, 字段
**Requirements**:
- 创建向后兼容的数据库迁移脚本
- 在测试环境验证迁移脚本
- 更新数据模型文档
- 备份重要数据（生产环境）

## Testing - 测试相关
**Triggers**: test, testing, unit, integration, e2e, 测试, 单元测试, 集成测试
**Requirements**:
- 确保测试覆盖率达到项目标准
- 运行完整的回归测试套件
- 更新测试文档和测试计划
- 验证功能在不同环境中的表现

## Deployment - 部署发布
**Triggers**: deploy, release, build, production, 部署, 发布, 构建, 生产环境
**Requirements**:
- 检查部署清单和发布说明
- 验证所有环境配置的正确性
- 准备回滚计划和故障恢复方案
- 监控部署后的系统状态

---

## 使用说明

### 添加新场景
按以下格式添加：

```markdown
## Your Scenario - 场景名称
**Triggers**: keyword1, keyword2, 中文关键词1, 中文关键词2
**Requirements**:
- 第一个工作流要求
- 第二个工作流要求
- 第三个工作流要求
```

### 场景检测
系统会扫描refined prompt中的关键词，匹配相关场景并添加对应的工作流要求。