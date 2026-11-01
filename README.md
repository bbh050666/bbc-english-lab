# BBC English Lab — BBC 英语精学 Skill

这份 Skill 将你的 **BBC 学习流程本身**变成可重复调用的英语教练：官方选材 → 语言与句型学习 → 听力理解 → 翻译与观点输出 → 逐项批改 → 长期学习档案。

## 每期会做什么

- 优先最近7天的 Six Minute English；主题偏社会学、心理学、AI、科技、教育、文化，必要时用注明日期的历史节目。
- 整理8–12个表达、2–3个结构，提炼3个核心表达、2个句型、1个论证技巧。
- 设计54分钟训练：14分钟首听复听、13分钟精读回忆、9分钟翻译、18分钟写作或辩论。
- 提供五题听力和三题翻译的直接回复模板；写作120–180词，或2–3轮辩论；先出题，收到回答后才批改。
- 依据实际答案给逐项反馈、五维评分、1优点2改进点及3–5分钟巩固任务；证据不足的维度记N/A。
- 记录真实材料、原始答案、反馈与复习。只有连续三次足够证据显示过易才建议正式升阶；用户也可随时试学更难材料。

新课固定六段：01 This Week's BBC Lesson；02 Language Bank；03 Grammar & Sentence Breakdown；04 Your 45–60 Minute Learning Plan；05 Writing / Debate Challenge；06 Weekly Progress。

## 文件

```text
bbc-english-lab/
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── lesson-workflow.md
│   ├── feedback-progress.md
│   └── archive-protocol.md
├── assets/BBC-learning-archive-template.md
└── README.md
```

## 安装与调用

解压 ZIP，把完整 `bbc-english-lab` 文件夹放进当前项目的 `.agents/skills/`，或个人目录 `~/.agents/skills/`；已有同名文件夹时先比较，不直接覆盖。目录与技能发现方式见 [OpenAI 官方技能文档](https://learn.chatgpt.com/docs/build-skills)。若技能列表未更新，重新启动再查看。

也可以从 [GitHub 仓库](https://github.com/bbh050666/bbc-english-lab) 使用 **Code → Download ZIP** 下载，解压后按上面的目录放置。私有仓库需要先登录有访问权限的账号。

下载或克隆仓库不会自动完成全局安装。Skill 为文字指令，无需额外运行脚本或 API key。新课实时选材需要可用的浏览／检索能力；更新文件需要可用的文件工具或资料库连接。

支持 `$` 调用的 Codex 界面可以直接输入：

```text
请用 $bbc-english-lab 开始一期54分钟的BBC精学。
优先最近7天的社会学、心理学、AI或教育主题。
先出题，不提前给答案；收到我的作答后再批改。
将材料与真实作答记录到 BBC learning english.md。
```

后续可以直接说：

- “继续上一期，我先提交 L1–L5：……”
- “这是 T1–T3 的翻译答案：……”
- “我选写作，这是原稿：……”
- “我选辩论，我支持这一方，第一轮观点是……”
- “带我复习反复错误，看看现在是否适合升级。”

## 学习档案

实际档案文件名是 **BBC learning english.md**，每期包含六部分：Learning Materials、Transcript、Language Bank、Listening Practice、Writing/Debate、Progress Tracking。课程草稿、用户原始回答、反馈和修订分别保留，不把备课当学习完成。

优先写入你指定且工具可访问的位置。如果没有 GPT 资料库写入工具，则提供当前项目 `outputs/BBC learning english.md` 本地文件，并明确它没有上传到 GPT 资料库；没有文件工具则提供可复制内容。只有实际写入并读回才报告保存成功。

[档案模板](assets/BBC-learning-archive-template.md)是空白结构，不代表已经学过一期。不要把用户记录写进已安装的 Skill 文件夹。

仓库只分发技能与模板。`.gitignore` 已排除默认学习档案、`outputs/` 和 `work/`，个人作答记录应继续保存在自己的学习位置。

## 真实来源与使用边界

具体节目和日期每次重新核验；不能播放音频时给播放入口，不声称听过。BBC 网站受抓取限制或YouTube字幕不可读时，改试其他官方路径／历史节目，或使用你提供的材料；没有材料就说明无法完成备课，不凭空生成原句。

Transcript 只有用户提供或明确许可允许时才保存全文；否则保存官方链接、允许短摘录和原创摘要。公开可下载不等于可全文转载；完整 BBC 原例句如不适合转载，给出处和原创语境释义，不伪造成原文。

这份 Skill 不保证提分，也不会凭三句翻译或一篇文章断言听力、口语等级。它会把可观察的表现、主观感受与尚未验证的能力分开记录。

## 本版本检查范围

已完成格式、引用路径和54分钟时长检查，并以自拟授权材料做离线应用试跑：生成课程、接收三句翻译、批改、建立并更新测试档案，写后读回核对原始答案、六部分结构及学习状态。测试记录与用户真实学习档案分开。

本环境未能完整抓取 BBC 官方课程页面，因此这次未完成实时最新节目选材实测，也未实际安装到全局目录。在线选材、播放和资料库写入仍取决于运行时工具与访问权限。
