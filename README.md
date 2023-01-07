# docs-sy-post-publisher

[思源笔记发布工具](https://github.com/terwer/src-sy-post-publisher) 使用帮助文档

![](https://img1.terwer.space/api/public/202301072138789.png)

## 参与贡献

如果你想帮助完善此文档，可按照以下步骤来进行：

1. `clone` 此项目到本地

    ```bash
    git clone git@github.com:terwer/docs-sy-post-publisher.git --depth 1
    ```

2. 直接修改 `content/<国际化>/` 目录里面的对应内容即可。例如：中文对应 `content/zh` 目录

3. 本地查看效果

   本文档基于 [HUGO](https://gohugo.io) 生成，可参考HUGO官方文档 [安装HUGO](https://gohugo.io/installation/macos/#homebrew) ， 使用以下命令查看效果：

   ```bash
   hugo server
   ```
   
   然后访问 http://localhost:1313 查看效果

4. 修改完成之后 `push` 到您自己的仓库，然后对 https://github.com/terwer/docs-sy-post-publisher 的 master 分支 发起 `pull request` 即可。`pull request` 合并完成之后，文档会自动构建完成并更新。

## 参考

https://github.com/vercel/community/discussions/38#discussioncomment-2719295

https://www.docsy.dev/docs/adding-content/navigation/#configure-algolia-docsearch

https://docsearch.algolia.com/docs/tips/

## 感谢

感谢 [Docsy](https://github.com/google/docsy) 项目提供的文档模板