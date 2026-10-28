# 本地开发与写作

本项目基于 [Firefly](https://github.com/CuteLeaf/Firefly)，保留原主题许可证与署名。

```powershell
pnpm install --frozen-lockfile
pnpm dev
```

本地访问 http://localhost:4321。

- 文章：`src/content/posts/`；运行 `pnpm new-post my-post` 创建文章。
- 站点配置：`src/config/siteConfig.ts`。
- 首页壁纸：`src/config/backgroundWallpaper.ts`。
- 个人介绍：`src/config/profileConfig.ts`。
- 关于页面：`src/content/spec/about.md`。

**此仓库公开：草稿、图片和历史提交都可被别人读取。不要存放私人笔记或凭证。**
主题自带示例文章标记为草稿，仅作为写作参考。

修改并提交到 master：
```powershell
git add src
git commit -m "content: update posts"
git push origin master
```

推送会通过 Request deployment 工作流通知私有部署系统。
公开工作流成功只表示通知已接受，实际构建与发布结果在私有仓库查看。
此仓库不保存服务器配置、SSH 密钥或部署日志。

发布前检查：`pnpm check`、`pnpm type-check`、`pnpm build`。
