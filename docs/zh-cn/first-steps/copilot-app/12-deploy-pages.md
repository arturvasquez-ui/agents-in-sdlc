---
title: "课程 12 - 使用 GitHub Pages 部署网站"
description: "使用 GitHub Copilot 应用配置 Pages 工作流、审查 pull request，并验证 Space Quiz 已成功上线。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

使用 GitHub Pages 部署 Space Quiz，让其他人也能访问。Copilot 可以准备工作流并指导部署，但你仍需负责审查更改并确认网站已上线。

在本课程中，你将：

- 请 Copilot 配置 GitHub Pages 部署。
- 在合并前审查工作流和 pull request。
- 跟进部署过程并验证已发布的网站。

## 场景

Space Quiz 已在 GitHub 存储库中，但用户还需要一种简单的试用方式。使用 GitHub Pages 发布这个单文件网站后，用户便可通过公共 URL 访问，而无需添加服务器或运行时依赖项。

## 请 Copilot 部署网站

在 `space-quiz` 的 Copilot 应用会话中发送以下提示：

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![三阶段示意图：已合并的 space-quiz pull request；GitHub Actions 的 Deploy website 运行成功，其中包含 Build website、Upload artifact 和 Deploy to Pages 步骤；以及已在 yourname.github.io/space-quiz/ 上线的 Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> 此提示会要求代理创建并合并 pull request，以及更改存储库的 Pages 设置。继续之前，请审查差异、部署权限和 GitHub 的任何审批请求。

## 审查工作流并验证部署

1. 确认只有在存储库尚无 README 时才添加了 README。
2. 审查 pull request 中的更改，包括工作流的构建和部署步骤。
3. 只有在必需的 pull request 检查全部通过后才进行合并。
4. 跟进 GitHub Actions 部署运行，直到成功完成。
5. 打开报告中的 URL，确认 Space Quiz 可以正常加载。

如果代理无法启用 Pages 或合并 pull request，请按照代理提供的具体说明操作。只有在部署成功且线上网站能够加载后，才将任务视为完成。

## 总结和后续步骤

Space Quiz 现已作为在线网站发布；你也亲自验证了部署，而不是只依赖代理的报告。继续学习[课程 13：审查和后续步骤][next-lesson]。

[next-lesson]: ../13-review/
