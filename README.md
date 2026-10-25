# qiniu-hackathon-xcanvas

七牛第五届 1024 Hackathon 作品仓库。

- 议题：用 XCanvas 制作《琅琊榜》第一集
- 作品：麒麟才子
- 成员：
  - zab1107
  - zhaohongqiang0144
  - niuyihang
- 仓库：https://github.com/zab1107/qiniu-hackathon-xcanvas

## 如何运行

这不是前后端服务，评委按下面复现即可。

1. 打开 Demo 视频：https://github.com/zab1107/qiniu-hackathon-xcanvas/releases/download/v1.0.0/qilin-demo-720p.mp4
2. 阅读剧本和角色卡：`docs/script.md`、`docs/characters.md`
3. 打开 XCanvas：https://dev-aicanvas.qnlinking.com/
4. 按 `docs/shots.md` 和 `docs/timeline.json` 生成并拼接 28 段分镜
5. 需要重导出时，按 `docs/reproduce.md` 把草稿导入剪映

详细步骤见 `docs/reproduce.md`。

## 演示

- Demo 视频（720p）：https://github.com/zab1107/qiniu-hackathon-xcanvas/releases/download/v1.0.0/qilin-demo-720p.mp4
- 备用（480p）：https://github.com/zab1107/qiniu-hackathon-xcanvas/releases/download/v1.0.0/qilin-demo-480p.mp4
- Release 页面：https://github.com/zab1107/qiniu-hackathon-xcanvas/releases/tag/v1.0.0
- 部署方式：XCanvas 生成分镜 + 剪映成片
- 演示账号：无

## 协作约定

- 所有变更必须通过 Pull Request 合入 `main`，禁止直推。
- 团队作品需要保留多人提交记录，不要最后一天一次性提交。
- 每人使用自己的 GitHub 账号，开 `feat/模块名` 或 `docs/说明` 分支。
- 截止时间：2026-10-26 09:00，之后仓库不能再有修改痕迹。

## codebase 说明

- 是否有 codebase：无
- 基线 tag：无

## 文档

- 架构设计：`docs/architecture.md`
- 剧本：`docs/script.md`
- 角色卡：`docs/characters.md`
- 分镜表：`docs/shots.md`
- 复现步骤：`docs/reproduce.md`
- 时间轴：`docs/timeline.json`
- PR 模板：`.github/PULL_REQUEST_TEMPLATE.md`
