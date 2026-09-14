# renovate
Shared Renovate presets for vodtv projects.

## Presets
- default: node-app
- node-app: Node.js application
- node-lib: Node.js library / SDK
- docker: Docker image project
- monorepo: PNPM monorepo

## Usage
### Default (node-app)
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>vodtv/renovate"]
}
```
## 示例：禁止对 GitHub Actions 执行 Pin 锁定版本
如果你不想 Renovate 把 `@v7` 自动锁定为 `v7.0.1` 这种精确版本，
可以在当前仓库的 `renovate.json` 增加 `packageRules`，**只关闭 pin，正常版本升级依旧保留**。

```json
{
  "packageRules": [
    {
      "matchDatasources": ["github-actions"],
      "matchUpdateTypes": ["pin"],
      "enabled": false
    }
  ]
}
