# MyTriliumNextNote

可以直接从 `document.db` 生成静态网页

## 如何使用（简而言之）

### 文件夹结构
- `.github` actions 任务流文件
- `site-assets` 需要添加的额外站点文件（如favicon.ico、robots.txt等）
- `trilium-data` 存放 document.db 文件

### 准备

- 在 `Trilium Notes` 中设置密码
- 在GitHub中新增仓库secrets，名为 `TRILIUM_PASSWORD`，内容写设置的密码
- Pages设置 Build and deployment 选择 `GitHub Actions`
- 将 document.db 文件放入 `trilium-data` 文件夹中
- 上传到GitHub仓库

### actions 任务流文件可选参数

- 笔记 ID：要发布为静态网页的笔记
- Trilium 服务端镜像，版本必须 >= 本地 Trilium 版本

本仓库的核心是 trilium-static-site.yml 工作流文件，不要连该文件都没有放入你的仓库就开始操作！