# 如何复现

这不是一个需要 `npm install` 的代码仓库。复现路径是：看剧本和角色卡，用 XCanvas 生成分镜，再按时间轴合成。

## 1. 看成品

- 720p：https://github.com/zab1107/qiniu-hackathon-xcanvas/releases/download/v1.0.0/qilin-demo-720p.mp4
- 480p：https://github.com/zab1107/qiniu-hackathon-xcanvas/releases/download/v1.0.0/qilin-demo-480p.mp4

## 2. 打开 XCanvas

- 平台：https://dev-aicanvas.qnlinking.com/
- 文档：https://dev-aicanvas.qnlinking.com/docs/

按 `docs/characters.md` 建角色，按 `docs/script.md` 写第一集，生成分镜视频。不要直接整集一次出片。

## 3. 对齐时间轴

`docs/timeline.json` 记录了 28 段镜头顺序和时长。新生成的镜头按 `clip_001` 到 `clip_028` 编号。

## 4. 剪映合成

1. 准备草稿包：`draft_content.json`、`draft_meta_info.json`、`timeline.json`、`media/clip_XXX.mp4`
2. 打开剪映专业版
3. 导入该草稿文件夹
4. 若提示媒体丢失，手动指向 `media/`
5. 检查声画后导出 mp4

剪映导入原文见 `docs/jianying-import.txt`。

## 5. 不要做的事

- 不要把成片 mp4 或 `media/` 提交进 git
- 不要直推 `main`
- 10/26 09:00 后不要再改仓库
