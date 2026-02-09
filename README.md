<img align="right" width="150" alt="logo" src="https://user-images.githubusercontent.com/5889006/190859553-5b229b4f-c476-4cbd-928f-890f5265ca4c.png">

# Hugo Theme Stack 启动模板

这是 [Hugo theme Stack](https://github.com/CaiJimmy/hugo-theme-stack) 的快速启动模板。它使用 [Hugo modules](https://gohugo.io/hugo-modules/) 功能来加载主题。

它包含基本的主题结构和配置。已设置 GitHub action 自动将主题部署到公共 GitHub 页面。此外，还有一个 cron 作业每天自动更新主题。

## 视频教程

如果您在设置过程中遇到困难，这里有一个视频教程，介绍如何使用此模板设置新的 Hugo 站点并将其部署到 GitHub Pages：https://www.youtube.com/watch?v=8qDdQQ6Ifxo

## 开始使用

1. 点击 *Use this template*，并在 GitHub 上创建名为 `<username>.github.io` 的仓库。（您也可以使用不同的仓库名称，但生成的网站将在 `https://<username>.github.io/<repository-name>` 上可用。）
![Step 1](https://user-images.githubusercontent.com/5889006/156916624-20b2a784-f3a9-4718-aa5f-ce2a436b241f.png)

2. 仓库创建后，创建与其关联的 GitHub codespace。
![Create codespace](https://user-images.githubusercontent.com/5889006/156916672-43b7b6e9-4ffb-4704-b4ba-d5ca40ffcae7.png)

3. 在等待 codespace 创建的同时，转到新创建仓库的 `Settings` -> `Pages`，并将 `Build and deployment` -> `Source` 设置为 `GitHub Actions`。
![Change build and deployment source](https://github.com/user-attachments/assets/192459bf-25d8-441e-8029-c108d789e449)

4. codespace 创建后，您可以在终端中运行 `hugo server` 来测试站点是否成功构建，并查看您的新站点。

5. 查看 `config` 文件夹中的配置文件。您可以根据需要编辑它们。确保更新 `config/_default/config.toml` 中的 `baseurl` 属性为您的站点 URL。例如，如果您的新仓库名为 `my-blog`，则 `baseurl` 应该是 `https://<username>.github.io/my-blog/`。

6. 编辑完成后，只需提交并推送即可。GitHub action 将自动将站点部署到与仓库关联的 GitHub 页面。

---

如果您不想使用 GitHub codespace，也可以在本地机器上运行此模板。**您需要在本地安装 Git、Go 和 Hugo extended。** 有关更多信息，请查看官方 Hugo 文档：https://gohugo.io/installation/

## 手动更新主题

运行：

```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v4
hugo mod tidy
```

> 此启动模板已配置为使用主题的 `v4` 版本。由于 Go module 的限制，一旦主题的 `v4` 或更高版本发布，您需要手动更新主题。（修改 `config/module.toml` 文件）

## 部署到其他静态页面托管服务

查看官方 Hugo 文档：https://gohugo.io/host-and-deploy/
