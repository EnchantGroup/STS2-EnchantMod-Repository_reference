# STS2 附魔模组引用仓库

本仓库通过 **Git Submodule** 引用独立维护的「杀戮尖塔 2」附魔相关的模组仓库，便于在其它工程或文档中固定版本、统一拉取。

## 子模块

| 路径 | 远程仓库 | 说明 |
|------|----------|------|
| `STS2-MoreEnchantStandalone/` | [Miooowo/STS2-MoreEnchantStandalone](https://github.com/Miooowo/STS2-MoreEnchantStandalone) | 不依赖 RitsuLib 的更多附魔 MOD（构建、安装与功能说明见该仓库 [README](https://github.com/Miooowo/STS2-MoreEnchantStandalone/blob/main/README.md)） |
| `MultiEnchantmentMod/` | [1939323749/MultiEnchantmentMod](https://github.com/1939323749/MultiEnchantmentMod) | 多附魔支持，提供API支持mod附魔多附魔。[文档](https://github.com/1939323749/MultiEnchantmentMod/wiki/MultiEnchantmentMod-Stack-%E7%B1%BB%E5%9E%8B%E4%B8%8E%E7%94%A8%E6%B3%95)） |

## 克隆本仓库

一次性拉取主仓库及所有子模块：

```bash
git clone --recurse-submodules <本仓库 URL>
```

若已克隆但未带子模块：

```bash
git submodule update --init --recursive
```

## 更新子模块到上游最新提交

在子模块目录内拉取，或在主仓库根目录执行：

```bash
git submodule update --remote STS2-MoreEnchantStandalone
```

更新后请在主仓库提交子模块指针变更（`STS2-MoreEnchantStandalone` 所指向的 commit），以便他人同步到相同版本。

## 修改子模块代码时

在 `STS2-MoreEnchantStandalone` 内开发与提交应推送到 [上游仓库](https://github.com/Miooowo/STS2-MoreEnchantStandalone)；本引用仓库只记录子模块应检出的 commit，不替代上游的开发流程。
