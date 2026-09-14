# Renovate Presets

自用 Renovate 配置预设仓库，多个项目可以直接复用，统一依赖更新策略，并且支持在单个项目按需覆盖规则。

## 使用方式
在你的项目根目录新建 `renovate.json`，通过 `extends` 引入本套预设。
下面提供**3套完整的 renovate.json 实际文件示例**，直接复制使用即可。

### 示例1：最简引入预设（新项目基础模板，推荐大多数场景）
只继承公共预设，不增加任何自定义覆盖规则，完全沿用 base.json 的全部策略。
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>vodtv/renovate"]
}
```
### 示例 2：引入预设 + 禁止本仓库 GitHub Actions Pin 锁定
不想 Renovate 把 `@v7` 自动锁定为 `v7.0.1` 这种精确版本。
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>vodtv/renovate"],
  "packageRules": [
     {
      "matchDatasources": ["github-actions"],
      "matchUpdateTypes": ["pin"],
      "enabled": false
     }
   ]
}
```
