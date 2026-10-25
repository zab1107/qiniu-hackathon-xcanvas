# 架构设计

## 1. 作品目标

- 议题：用 XCanvas 制作《琅琊榜》第一集
- 作品名：麒麟才子
- 要解决的问题：把一集古装剧拆成可生成的角色、剧本和分镜，用 XCanvas 产出镜头，再合成可看的成片。
- 目标用户：需要快速验证短剧/漫剧生成流程的制作人员。
- 3 天内必须跑通的最小闭环：剧本 -> 角色 -> XCanvas 分镜视频 -> 剪映成片 -> GitHub Release。

## 2. 模块规格

| 模块 | 职责 | 输入 | 输出 | 负责人 |
| --- | --- | --- | --- | --- |
| 剧本与角色 | 固定第一集故事线和出场人物 | 议题、原剧情节 | 剧本、角色卡 | zab1107 |
| XCanvas 生成 | 按角色和剧本生成分镜视频 | 角色卡、剧本、分镜提示 | 28 段 clip | niuyihang / zhaohongqiang0144 |
| 成片合成 | 按时间轴拼接、补声、导出 | clip、剪映草稿 | 1080p 成片 | zab1107 |
| 交付 | README、架构文档、Release | 成片和文档 | 评委可打开的仓库 | zab1107 |

数据流：

```
剧本 / 角色卡
        |
        v
XCanvas 生成 28 段分镜
        |
        v
剪映草稿包（timeline.json + media/clip_XXX.mp4）
        |
        v
成片 mp4 -> GitHub Release v1.0.0
```

## 3. 分工

| 成员 | GitHub | 模块 | 10/24 | 10/25 | 10/26 08:30 前 |
| --- | --- | --- | --- | --- | --- |
| 张 | zab1107 | 仓库、剪映成片、文档、Release | 建仓、保护 main、走 PR | 合成成片、上传 Release、补文档 | 冻结仓库 |
| 赵 | zhaohongqiang0144 | XCanvas 分镜与素材 | 角色/场景素材 | 补齐失败镜头以外的分镜 | 不再提交 |
| 牛 | niuyihang | XCanvas 分镜与素材 | 生成分集视频 | 与成片时间轴对齐 | 不再提交 |

本次仓库提交由 zab1107 代提 PR。XCanvas 侧素材仍由另外两人在平台上生成。

## 4. 技术选型

- 生成平台：XCanvas（https://dev-aicanvas.qnlinking.com/）
- 文档：https://dev-aicanvas.qnlinking.com/docs/
- 合成：剪映专业版
- 交付：GitHub 仓库 + Release 成片
- 无自研前后端，无 codebase。基线 tag 无。

## 5. 开发规范

1. `main` 受保护，所有代码和文档都走 PR。
2. 分支命名：`feat/xxx`、`fix/xxx`、`docs/xxx`。
3. 大视频不进 git，放 GitHub Release。
4. 10/26 09:00 后禁止任何仓库修改。

## 6. 交付清单

- [x] Demo 视频（Release v1.0.0）
- [x] 架构设计文档（本文件）
- [x] 如何运行 / 如何复现（README + `docs/reproduce.md`）
- [x] 剧本、角色、分镜表
- [ ] 可在线打开的 XCanvas 项目（评委用文档和成片复核）
