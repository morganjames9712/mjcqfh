汇众官网娱乐【Q-——333307——】汇众官网娱乐【 辋芷《888yx●vip》 】
汇众官网娱乐【Q-——333307——】汇众官网娱乐【 辋芷《888yx●vip》 】

 我用 GitHub Action 自动部署 Hexo，终于告别手动敲命令了

折腾博客这么久，每次写完文章都要自己敲 `hexo g` 再 `hexo d`，偶尔忘了部署，页面还是旧的。直到我把部署流程交给 GitHub Action，才算真正解放双手。

 为什么建议你试试 GitHub Action

Hexo 部署到 GitHub Pages 本身不复杂，但手动流程有几个痛点：

- 容易忘记部署，文章写完没上线
- 本地环境不一致，换个电脑就要重装 Node.js
- 多分支管理麻烦，源码和静态文件容易混

GitHub Action 可以把这些全部自动化：你只管 `git push` 源码，剩下的构建、部署、推送都由云端完成。

 核心配置思路

在仓库根目录创建 `.github/workflows/deploy.yml`，核心逻辑分三步：

1. 触发条件：监听 `main` 分支的 push 事件
2. 构建环境：拉取 Node.js 环境，安装 Hexo 依赖
3. 部署动作：生成静态文件，推送到 `gh-pages` 分支

我在配置里加了缓存依赖的步骤，构建速度从原来的 2 分钟降到 40 秒左右，这个优化值得做。

 一个容易踩的坑

用 `Secrets` 存部署令牌时，记得在仓库设置里配置 `GH_TOKEN`，权限要选 `repo` 和 `workflow`。我之前只给了 `repo` 权限，结果 workflow 文件更新不了，排查了半天。

 互动一下

你现在部署博客用的是什么方式？是手动敲命令，还是已经在用 CI/CD 了？遇到过哪些坑？欢迎在评论区聊聊。

如果你还没试过 GitHub Action，建议按上面的思路配一个，跑通之后再看日志，会更有感觉。下一篇我会聊聊怎么用 GitHub Action 做自动检查图片压缩，记得关注。

相关推荐：

https://github.com/carlsonrobert4933/odnuoh/blob/main/2026%E7%A7%91%E6%8A%80%E8%A7%A3%E6%9E%90%EF%BC%9A%E6%B1%87%E4%BC%97%E5%AE%98%E7%BD%91%E6%B5%8B%E9%80%9F_%E5%88%AE%E4%B8%B6%E6%8B%B1%E5%A9%AA%E5%A3%ACSFZZG.md

<img src="https://i.postimg.cc/sD9qt00C/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(86).png" />

相关推荐：

https://github.com/carlsonrobert4933/odnuoh/commit/9385bc4c365ab29d2832014695717a00abb7a88d

<img src="https://i.postimg.cc/59zZmtBW/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(84).png" />
相关推荐：

https://github.com/howardpaul4373/ojtabp/blob/main/%E6%96%87%E5%A8%B1%E5%89%8D%E6%B2%BF%E8%B5%84%E8%AE%AF%EF%BC%9A%E6%B1%87%E4%BC%97%E5%AE%98%E7%BD%91%E7%BD%91%E5%9D%80_%E7%89%A1%E7%99%BE%E6%8B%93%E8%8D%A3%E6%92%82KQKKK.md

<img src="https://i.postimg.cc/sD9qt00C/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(86).png" />
相关推荐：

https://github.com/howardpaul4373/ojtabp/commit/47e1b3d5fdc17ca019b4b570257e6ad93a06d50a

<img src="https://i.postimg.cc/j5pBbVrM/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(82).png" />

资讯来源：新华网、人民网、央视新闻、中新网、凤凰网、澎湃新闻、界面新闻、新浪新闻、搜狐网、财新网、观察者网、第一财经等主流平台，以独树一帜的观察视角与扎实的深度报道能力，在资讯领域收获广泛关注。
