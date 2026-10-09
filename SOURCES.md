# 源与校验

所有上游来源均公开可验证，哈希与 `recipes/<版本>/PKGBUILD` 的 `b2sums` 一致。

## 内核源码 tarball

来自 `CachyOS/linux` GitHub Releases，URL 模板：

```
https://github.com/CachyOS/linux/releases/download/cachyos-<ver>/cachyos-<ver>.tar.gz
```

| 版本 | 文件 | b2sum (blake2b-512) |
|---|---|---|
| 7.2.9-2 | cachyos-7.2.9-2.tar.gz | `8a545c8da5cc1e0d803db9f761ee159733c963b40c594ba74f3723eab68abfd7e7a4ac92139a064cff65b0a0c742bf6989c5d05cd98f057a2ad9efd154c7df25` |

## 内核配置种子

`recipes/<版本>/config`：

```
7f4f37039be593d72170f6f0ca7fd29b2ea3cfef3237aa8e374a0738de01b11b57fdfa289eb184044cd677a94d1a43fdb99e3ce25a89b200ac3f807524de5b02
```

## 内核补丁

| 文件 | 上游 URL | b2sum |
|---|---|---|
| dkms-clang.patch | `https://raw.githubusercontent.com/cachyos/kernel-patches/master/7.2/misc/dkms-clang.patch` | `c992567bd7dd8553432be496ffa1c17e2f5ebe9c7edb51945cf977e1b742dd6517c210d8843bb82744ca705efd07f8027cd7dde41b50215ebd707a34aa81462e` |
| 0001-bore-cachy.patch | `https://raw.githubusercontent.com/cachyos/kernel-patches/master/7.2/sched/0001-bore-cachy.patch` | `03b6d236610ae00db9395819aa7578860f45ce10839fbdcee80fb8e9e9c8810896d20680c63e43c416ae23b371efd737bc0a14831e1f7d8111578c1f65bda68f` |

> PKGBUILD 中这些 URL 带 `https://ghfast.top/` 镜像前缀（便于国内拉取），b2sum 校验一致。
