# AI 生图 Skill、Prompt 与 Agent 资源

> 更新时间：2026-09-16
>
> 本文面向个人创作，整理 ChatGPT Images 与 Midjourney 相关的开源 Prompt 库、Agent Skill 和创作工作流。开源仓库不等于模型权重开源；使用前仍应检查许可证、依赖、账号安全和第三方平台条款。

## 快速结论

- 日常把想法变成可执行提示词：[`PromptAgent`](https://github.com/Shinning1010/PromptAgent)
- 想研究 ChatGPT 图像 API、编辑和 Agent：[`gpt-image-cookbook`](https://github.com/eugeniughelbur/gpt-image-cookbook)
- 想看最可靠的模型方法：[`OpenAI Cookbook`](https://github.com/openai/openai-cookbook)
- 想做分镜、系列视觉和美术指导：[`Omni-Art-Skills`](https://github.com/gracetey-zhang/Omni-Art-Skills)
- 想研究 Midjourney 的参考图、风格和迭代：[`midjourney-cc-skill`](https://github.com/justinperea/midjourney-cc-skill)
- 想快速复制 Midjourney 示例和参数：[`awesome-midjourney-v7-example-prompts`](https://github.com/Pixmind-io/awesome-midjourney-v7-example-prompts)
- 想让 Agent 为不同模型改写 Prompt：[`prompt-master`](https://github.com/nidhinjs/prompt-master)
- 想做系列图片并进行视觉质检：[`paper-signal`](https://github.com/jiahuiqu17/paper-signal)
- 想从带示例图的社区库检索 Prompt：[`ai-image-prompts-skill`](https://github.com/YouMind-OpenLab/ai-image-prompts-skill)

## 第一梯队：建议优先保留

### 1. OpenAI Cookbook

仓库：<https://github.com/openai/openai-cookbook>

相关材料：[`image-gen-models-prompting-guide.ipynb`](https://github.com/openai/openai-cookbook/blob/main/examples/multimodal/image-gen-models-prompting-guide.ipynb)

官方方法资料，适合学习：

- 结构化提示词
- 参考图的角色分工
- 图像编辑和局部修改
- 多轮迭代
- 文字、构图和身份保持
- API 调用方式

它不是简单的“万能提示词合集”，而是最适合作为基础规范的资料。

### 2. gpt-image-cookbook

仓库：<https://github.com/eugeniughelbur/gpt-image-cookbook>

这是一个较完整的开源图像 Agent 工程，包含：

- Prompt Gallery
- `SKILL.md` Agent Runbook
- Python CLI
- GPT Image API
- 参考图编辑
- 局部重绘和多参考图流程
- OpenAI、Imagen、Flux 的统一抽象

注意：项目目前主要围绕 `gpt-image-2` API，不等于直接控制 ChatGPT 网页里的 Images 2.5；需要 API Key，图片生成调用会产生费用。项目许可证为 MIT。

### 3. PromptAgent

仓库：<https://github.com/Shinning1010/PromptAgent>

这是一个轻量 Codex Skill，适合个人使用：

- 把一句想法扩展为专业提示词
- 区分身份参考、风格参考、构图参考和场景参考
- 生成正向和负向提示词
- 支持人像、产品、街拍、旅行、时尚等场景
- 支持后续修改和迭代

它更像“创意提示词助手”，不负责替你搭建完整的生图基础设施。仓库说明为非商业创作方向，使用前应自行确认当前许可证和用途限制。

### 4. Omni-Art-Skills

仓库：<https://github.com/gracetey-zhang/Omni-Art-Skills>

偏创意导演和视觉生产流程，包含：

- `creative-production-pipeline`：从故事或大纲组织完整视觉流程
- `script-to-shot-table`：把脚本转换成分镜和镜头表
- `image-art-direction`：分析参考图、规划风格、审查候选图

适合连续角色、系列图片、分镜和视觉叙事；不适合只想输入一句话马上生成单张图的人。

## Midjourney 专项资源

### 5. Midjourney CC Skill

仓库：<https://github.com/justinperea/midjourney-cc-skill>

它将 Midjourney 创作拆成：

```text
分析目标图
→ 拆分主体、光线、颜色、材质、构图、情绪和风格
→ 选择纯 Prompt、--sref 或参考图方案
→ 生成并评分
→ 根据差距进行 Vary、重写或局部编辑
```

适合研究如何建立 Midjourney 的可复用创作流程。注意：项目中的部分参数说明偏向 V7，而 Midjourney 当前默认版本已经更新到 V8.2，使用时应以[官方版本文档](https://docs.midjourney.com/hc/en-us/articles/32199405667853-Version)为准。

### 6. Midjourney Prompt Examples

仓库：<https://github.com/Pixmind-io/awesome-midjourney-v7-example-prompts>

包含人像、摄影、建筑、产品、动漫和电影感提示词，并整理了 `--ar`、`--s`、`--c`、`--sref` 等参数示例。仓库采用 CC0，但主要针对 V7，适合学习结构，不宜直接当作 V8.2 的参数基准。

## Prompt 库补充

- [`awesome-gpt-image-2-5-prompts`](https://github.com/youart-open-source/awesome-gpt-image-2-5-prompts)：150 个分类 Prompt，覆盖海报、产品、人像、UI、信息图和编辑任务。
- [`awesome-gpt-image`](https://github.com/ZeroLu/awesome-gpt-image)：GPT Image 2/2.5 提示词和案例合集。
- [`ai-visual-prompt-cookbook`](https://github.com/pcedison/ai-visual-prompt-cookbook)：用 JSON 组织可复用的视觉风格模板。

## 近期候选：通用 Prompt 与视觉生产

### 7. Prompt Master

仓库：<https://github.com/nidhinjs/prompt-master>

通用 Prompt Skill，能够根据目标工具选择不同的提示词结构，覆盖 ChatGPT、Midjourney、Flux、Stable Diffusion 和 ComfyUI 等。它更适合做“模型适配层”，不是独立的生图模型或风格生成器。仓库采用 MIT 许可证，社区规模较大。

### 8. Paper Signal

仓库：<https://github.com/jiahuiqu17/paper-signal>

面向视觉创作的 Agent Skill 集合，提供美术指导、系列图片生产和结果审查。它适合把参考图、风格系统、主体保持和生成后 QA 组织成一个可复用流程；仓库说明中标注了 Codex Desktop 的端到端参考运行时。仓库不附带模型或 API Key。

### 9. AI Image Prompts Skill

仓库：<https://github.com/YouMind-OpenLab/ai-image-prompts-skill>

面向多个图像模型的 Prompt 推荐 Skill，依赖带示例图的社区图库。它适合找灵感和风格案例，但“支持所有模型”应理解为 Prompt 可迁移，而不是每条 Prompt 在每个平台都能得到相同结果；建议作为检索型补充，而不是质量保证层。

提示：很多 GPT Image 2.5 Prompt 库是在 2.5 发布前收集的，应当把它们当作可改写的案例，而不是保证能复现的官方模板。

## 推荐安装和学习顺序

### 不写代码

1. 先读 OpenAI Cookbook 的图像提示词章节。
2. 使用 PromptAgent，把自己的中文想法改写成结构化 Prompt。
3. 用 ChatGPT Images 2.5 生成和多轮修改。
4. 使用 Midjourney Prompt Examples 学习 `--ar`、`--sref` 和风格控制。

### 想做 Agent 或自动化

1. 先看 `gpt-image-cookbook` 的 `SKILL.md` 和 Gallery。
2. 再看 `Omni-Art-Skills` 的分镜和美术指导拆分方式。
3. 把自己的常用 Prompt、参考图角色和检查清单整理成独立 Skill。
4. Midjourney 自动化只做个人实验，避免把登录信息交给来源不明的脚本。

## 通用提示词骨架

```text
Use case: <用途>
Asset type: <最终载体>
Primary request: <主体和动作>
Input images: <图片1的角色；图片2的角色>
Scene/backdrop: <环境>
Style/medium: <摄影、插画或 3D>
Composition/framing: <景别、视角、主体位置、留白>
Lighting/mood: <光线和情绪>
Text (verbatim): "<必须原样出现的文字>"
Constraints: <必须保留的内容>
Avoid: <不要出现的内容>
```

实践原则：先把主体、空间关系和约束说清楚，再补风格词；每轮只修改一个重点；涉及参考图时明确每张图负责什么；文字必须逐字放在引号中。

## 风险和维护提示

- Prompt 库、Skill、Agent 和模型权重是不同层次的资源，不要混为一谈。
- 使用第三方 CLI 前检查脚本是否读取、上传或持久化本地图片和环境变量。
- API Key 只通过环境变量传入，不写进 Prompt、README、日志或 Git 历史。
- Midjourney 和 ChatGPT 都是云端服务，隐私照片不要默认上传。
- 版本更新会改变参数和效果；使用前重新查看官方文档和仓库最近提交。
