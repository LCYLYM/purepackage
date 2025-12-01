# purepackage

专门用于云端构建的仓库：
- 在 Issues 中上传 AI Studio 导出的 zip
- 打上指定标签（例如 `build-zip`）
- GitHub Actions 自动下载附件，后续会在这里完成 exe / apk 构建

当前版本：
- 已实现：
  - 监听 issue 事件，解析正文中的 zip 附件链接
  - 下载 zip 文件到工作目录
  - 在 issue 中回复 "已收到构建请求" 并打上 `built` 标签，保证不会重复构建
- TODO：
  - 接入实际的打包逻辑（调用 Electron / Android 构建脚本生成 exe / apk）
