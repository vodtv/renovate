# renovate-config
集中管理的Renovate共享预设仓库

## 环境预设列表
- default: base 基础配置
- dev: 开发环境
- test: 测试环境
- prod: 生产环境

## 在业务仓库如何引用
### 方式1：使用默认base
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>你的用户名/renovate-config"]
}
