# Retake 插件目录

这是一个轻量、人工维护的 Retake Package GitHub 源码目录。

它不是 Registry 或插件市场：不托管 Package archive、不自动解析依赖、不自动执行更新、不做排名，
也不替代插件仓库自己的 License、安全审查和权限确认。

## 从 GitHub 安装

```text
github:<owner>/<repository>@<ref>#subdirectory=<package-root>
```

Retake 会把 GitHub ref 解析为 exact commit，只验证和构建 manifest 声明的文件，并在 Workspace
lock 中记录 exact commit 与 content digest。使用 `main` 等移动分支可以接收更新通知；使用 tag
或 commit 表示有意固定版本。更新始终需要用户显式执行。

## 官方 Package

### Retake Image Studio

- 仓库：[retake-tools/image-studio](https://github.com/retake-tools/image-studio)
- Package ID：`design.retake.image-studio`
- Package root：`plugin`
- 开发源：`github:retake-tools/image-studio@develop#subdirectory=plugin`
- License：Apache-2.0
- 状态：官方，随 Retake Whiteboard 离线分发

### Retake Video Studio

- 仓库：[retake-tools/video-studio](https://github.com/retake-tools/video-studio)
- Package ID：`design.retake.video-studio`
- Package root：`package`
- 开发源：`github:retake-tools/video-studio@develop#subdirectory=package`
- License：Apache-2.0
- 状态：官方，随 Retake Whiteboard 离线分发

首次公开 release promotion 完成后再列出稳定 `main` 安装命令。Whiteboard bundled Package
继续保证首次离线可用。

## 提交插件

通过 Pull Request 增加条目，并提供：

- 仓库 URL、Package ID；
- 非仓库根目录时的 Package root；
- 推荐移动 ref 和可选固定 release ref；
- License；
- Capability 简介；
- 最近验证日期与兼容 Whiteboard 版本。

进入目录不等于获得代码信任。Whiteboard 激活前仍会验证源码、权限、Package identity、
兼容范围和 content digest。
