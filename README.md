# CDN 加速文件存放地

本仓库用于存放需要通过 CDN 加速访问的静态文件（图片、CSS、JS 等），借助 jsDelivr 和 Staticaly 两大免费 CDN 服务，实现全球加速分发。

> **注意：** GitHub 仓库对文件大小有限制（单文件不超过 100MB，仓库总大小建议不超过 1GB）。详见 [GitHub 磁盘配额说明](https://docs.github.com/cn/github/managing-large-files/what-is-my-disk-quota)。

---

## 使用方式

### jsDelivr

官网：[https://www.jsdelivr.com](https://www.jsdelivr.com)

jsDelivr 是一个免费、快速、可靠的开源 CDN，自 2012 年运营至今，拥有超过 540 个全球节点，由 Cloudflare、Fastly、G-Core Labs、bunny.net 等多家赞助商提供支持。

**URL 格式：**

```
https://cdn.jsdelivr.net/gh/user/repo@version/file
```

**使用示例：**

```bash
# 加载指定版本（tag、commit 或 branch）的文件
https://cdn.jsdelivr.net/gh/yiktt/cdn@master/README.md

# 使用版本范围代替精确版本号
https://cdn.jsdelivr.net/gh/yiktt/cdn@1/README.md

# 省略版本号获取最新版本（不建议在生产环境使用）
https://cdn.jsdelivr.net/gh/yiktt/cdn/README.md

# 在任意 JS/CSS 文件名后加 ".min" 获取压缩版本（若不存在则自动生成）
https://cdn.jsdelivr.net/gh/yiktt/cdn@master/style.min.css

# 在路径末尾加 "/" 获取目录列表
https://cdn.jsdelivr.net/gh/yiktt/cdn/
```

> 提示：jsDelivr 支持加载任意 GitHub release、commit 或 branch 的文件。对于支持 npm 的项目，官方建议优先使用 npm 方式引用。

---

### Staticaly

官网：[https://statically.io](https://statically.io)

Staticaly 是一个免费、快速的全球 CDN，由 bunny.net 和 Cloudflare 提供支持，支持 GitHub、GitLab、Bitbucket 及 npm 等平台的静态文件分发。

> ⚠️ **注意：** Staticaly 目前在中国大陆地区无法访问，请酌情选择使用。

**URL 格式：**

```
https://cdn.statically.io/gh/:user/:repo@:tag/:file
```

**使用示例：**

```bash
# 加载指定版本（tag、commit 或 branch）的文件
https://cdn.statically.io/gh/yiktt/cdn@master/README.md

# 加载 GitLab 仓库文件
https://cdn.statically.io/gl/:user/:repo@:tag/:file

# 加载 Bitbucket 仓库文件
https://cdn.statically.io/bb/:user/:repo@:tag/:file

# 加载 GitHub Gist 文件
https://cdn.statically.io/gist/:user/:gist_id/raw/:commit/:file

# 加载 npm 包文件
https://cdn.statically.io/npm/:package@:version/:file
```

> ⚠️ **Important Notice：** 由于滥用和高流量，Staticaly 的 `/img/` 端点已被禁用。请合理使用 Statically 服务。

---

<p align="center"><sub>📄 本 README 由 AI 生成</sub></p>
