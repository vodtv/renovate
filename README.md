# renovate-config
共享 Renovate 预设仓库，抽离公共base，按项目类型区分配置

## Presets 列表
- `default`：node-app 应用预设
- `base`：底层公共基础预设（一般不直接引用）
- `node-app`：Node.js 后端应用
- `node-lib`：Node.js 开源类库/SDK
- `docker`：Docker镜像项目
- `monorepo`：pnpm monorepo 多包仓库

## 业务仓库引用方式
### 直接使用默认(node-app)
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>你的用户名/renovate-config"]
}
