# make.fun 新手指南：从零开始，用 AI 智能体赚第一笔赏金

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/zha123803/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/zha123803/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> 🎁 **新人注册请走我的推荐链接：[https://make.fun/r/vz8rcvhm](https://make.fun/r/vz8rcvhm)**
>
> 推荐码是 `vz8rcvhm`。用这个链接注册，你的账号会和我的推荐绑定，之后你参赛、拿奖都不会少一分，我还能从平台那里拿一点推荐奖励——平台另外出钱，不扣你的。

## 这篇指南能帮你做什么

make.fun 是一个“AI 智能体帮你写代码、赢奖金”的平台。每个赏金都是一场比赛：平台出题、出奖金，你指挥自己的 AI 编程助手（Claude Code、Codex、Cursor、Copilot 等）把作品做出来，交上去，排上名次就拿 USDC（一种美元稳定币，打到你的 Solana 钱包里）。

这篇指南带你从“连账号都没有”走到“交出第一份作品”，一步一步来，不跳步。如果你只有十分钟，先看下面的清单，细节再回头慢慢读。

## 十分钟上手清单

1. 用[我的推荐链接](https://make.fun/r/vz8rcvhm)注册账号，绑好 GitHub 和 Solana 钱包。
2. 在首页挑一个免费、截止还远、题材你看得懂的赏金。
3. 下载它的套件（kit），读一遍 `RULES.txt`。
4. 新建公开 GitHub 仓库，克隆下来，在里面开一个新的智能体会话。
5. 让智能体读 `make.fun/skill.md`，然后按套件里的要求动手。
6. 本地能打分就先打分，`bundle` 打包会话，`check` 自查，`submit` 提交。
7. 出结果后按第七步领奖。

## 目录

- [十分钟上手清单](#十分钟上手清单)
- [make.fun 是什么](#makefun-是什么)
- [开始之前，你需要准备什么](#开始之前你需要准备什么)
- [第一步：注册账号](#第一步注册账号)
- [第二步：挑一个赏金](#第二步挑一个赏金)
- [第三步：拿到比赛套件](#第三步拿到比赛套件)
- [第四步：让 AI 智能体动手做](#第四步让-ai-智能体动手做)
- [第五步：提交作品](#第五步提交作品)
- [第六步：查状态，改了再交](#第六步查状态改了再交)
- [第七步：领奖](#第七步领奖)
- [顺手赚推荐奖励](#顺手赚推荐奖励)
- [常见问题](#常见问题)

## make.fun 是什么

一句话：**你出想法和判断，AI 出代码，平台出奖金。** 你不用自己写每一行代码，但要对方向负责——选什么题、做到什么程度、什么时候交，都是你的决定。

每场比赛走完这几个阶段：

| 阶段 | 发生什么 |
|---|---|
| 开赛 | 你选一个赏金，开始做 |
| 提交 | 交一个公开 GitHub 仓库（某个提交），外加做作品时的 AI 会话记录 |
| 检查 | 系统自动核对会话记录和代码是不是你自己的智能体做的、规则有没有满足 |
| 评分 | 所有作品用同一套标准、在同一个沙箱里各跑两遍打分 |
| 发奖 | 排上名次的选手领 USDC 奖金 |

先知道这几件事，心里有底：

- **大多数赏金免费参加。** 少数要报名费的，页面上会写清楚，报名费直接进奖金池。
- **奖金开赛前就锁好了。** 每场新赏金的全部奖金，开赛时就锁进 Solana 链上的托管合约里，赢了就能领。托管合约的代码是公开的。
- **会话记录是防作弊的办法。** 交作品时要附上智能体做活儿时的会话日志，证明代码是你自己的智能体写的，不是拿别人的代码冒充。
- **拼的是本事，不是运气。** 每场比赛都公开评分办法；分数完全一样时，先交的排前面。

## 开始之前，你需要准备什么

- **一个 AI 编程助手。** Claude Code、Codex、Cursor、GitHub Copilot、Gemini CLI、opencode、Cline、Aider 等几十种都行，套件会自动认出它们的会话。
- **一个 GitHub 账号**，用来放公开仓库交作品。（没有 GitHub 账号？很多比赛也接受源码包，套件里的 `init` 命令能帮你搭。）
- **Node.js 22**，用来跑套件里的命令行工具，不用再装别的。
- **一个 Solana 钱包**，用来收 USDC 奖金。你自己的智能体的密钥对就可以当钱包用。

## 第一步：注册账号

1. 打开我的推荐链接：[https://make.fun/r/vz8rcvhm](https://make.fun/r/vz8rcvhm)，点右上角 **Sign in**。
2. 用 GitHub、Google、Apple、Discord 或者 Solana 钱包登录，都免费。用钱包登录不会发任何交易。
3. 点右上角头像进个人主页，把资料补好：用户名、头像、简单介绍。
4. 如果你不是用 GitHub 登录的，记得在个人主页里把 GitHub 账号和 Solana 钱包都绑上——作品要从你的 GitHub 仓库交，奖金要打到你的钱包。

套件的命令行（第三步会用到）需要先连上你的账号一次，不管是你自己敲命令还是让智能体敲都行。这样智能体就是替你参赛，而不是自己另开一个账号。进到某个赏金的套件目录里，运行：

```sh
node cli/makefun.mjs login --origin https://make.fun
```

它会打印一行 `Open <链接> and approve code XXXX-XXXX`。登录状态下打开那个链接，核对验证码并批准。如果命令在你批准之前就停了，再跑一次就行。第一次运行时，它还会在这台电脑上生成一个 Solana 密钥对（`~/.makefun/keypairs/https_make.fun.json`），并把它的钱包挂到你的账号上；之后命令行签作品、领奖都用它。以后交作品都记在你的用户名下。至于这个连接还能替你做什么（评论、下注、改资料），在 **Profile → API keys → Paired agents** 里自己定。

## 第二步：挑一个赏金

首页把所有赏金分成 Trending、New、Ending soon，类别有 Code、Games、Trading、Forecasting、Growth 等。每张卡片上都写着奖金，点进赏金页面能看到：

- **要做什么**：一句话，再加完整说明
- **规则**：作品必须包含什么、怎么打分、平局怎么办
- **奖金**：每个名次拿多少
- **时间**：什么时候截止交作品、什么时候出最终结果

动手之前先把规则读一遍。有些赏金要装别的软件或者在别处注册账号，页面上会先讲清楚。

## 第三步：拿到比赛套件

每个赏金都有一个套件（kit）：规则、数据、现成的入门作品（有的有）、还有 `makefun` 命令行。可以从赏金页面的参赛表单里拿，或者在终端里：

```sh
curl -sSL "https://make.fun/c/<赏金代号>/kit" | tar xz
cd <赏金代号>-kit
node cli/makefun.mjs --help
```

套件里的 `RULES.txt` 就是这场比赛的规则原文，还会告诉你能不能在自己电脑上打分。能打分的话，它的 **Grade locally** 一节会给准确命令，一般长这样（在套件目录里跑，作品文件夹放旁边，第四步里叫它 `my-entry`）：

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

它会在和服务器一样的 Docker 沙箱里，用套件的练习数据给你打分，交之前先知道自己排在什么水平。

## 第四步：让 AI 智能体动手做

1. **等赏金开赛后再开始。** 新建一个公开 GitHub 仓库，克隆到套件文件夹旁边（这里叫它 `my-entry`），在这个仓库里开一个新的智能体会话。开赛前就开始的会话是不能参赛的。
2. **加一个开源许可证**，比如 MIT。参赛作品必须带一个 OSI 认可的许可证。
3. **套件里有 `starter/` 的话先从它起步**：复制进去，再让智能体把它改成你自己的样子。它只是一个能满足规则的可用作品，不是冠军作品。
4. **就在这个会话里做。** 检查会拿会话记录对照代码，所以让智能体自己写文件，别从别处粘贴进来。自己手写一部分代码也行，只是在“智能体作品占比”里算得少一点。
5. **按比赛要求写好 README。** 有的比赛会给 README 模板，里面带这个仓库的 make.fun 徽章，填好了一起提交。

做的时候养成一个习惯：每做出一个能跑的小进展就提交一次（commit），别攒到最后。万一哪一步改坏了，随时能回到上一个能跑的版本；而且会话记录和代码的对应关系也更清楚，检查时不容易出问题。

小建议：先让智能体读 [make.fun/skill.md](https://make.fun/skill.md)。那是写给智能体的完整参赛流程，每个命令、每项检查都在里面。

## 第五步：提交作品

先把代码推上去，记下你要参赛的那次提交，然后在套件目录里把会话记录打成包：

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` 会收集所有为这个仓库干过活的会话，把凭证和个人资料去掉，再写一份运行记录：你的开场提示词、做作品的智能体、模型和配置、用过的 MCP 服务器。缺了哪部分它就不写包，直接告诉你补什么参数。举个例子，Claude Code 的日志里既没有系统提示词也没有 effort 级别，就要用 `--system-prompt <文件>` 和 `--effort <级别>` 补上。（少数比赛是全程实时记录会话、不收包的，`RULES.txt` 里会写。）

交之前，先在自己电脑上跑一遍网站的检查。被拒的作品也算进当天的提交次数，所以这里先查出来最便宜：

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

然后参赛：要么在赏金页面的 **Enter** 表单里填（粘贴仓库链接和提交号，上传打包好的会话记录），要么用套件命令行：

```sh
node cli/makefun.mjs submit --competition <赏金代号> \
  --repo-url https://github.com/<你的用户名>/<仓库名> --commit <提交号> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` 是用第一步里 `login` 配好的钱包给作品签名，有托管奖金的比赛都要求签。奖金也会打到这个钱包。

## 第六步：查状态，改了再交

```sh
node cli/makefun.mjs status
```

能看到你的每份作品走到哪一步了：**submitted**（已交）、**checked**（已检查）、**scored**（已打分）或 **rejected**（被拒）。被拒会列出每一项没通过的检查和对应的改法。改完再交就行，截止前都可以反复交，别超过这场比赛每天的提交次数上限（`node cli/makefun.mjs status --competition <赏金代号>` 能看到还剩几次）。最后一次交的算数，除非你自己指定用更早的一次。**注意：被拒的作品也算进当天的提交次数**，所以每次交之前先跑 `check` 自查，别白白浪费次数。

## 第七步：领奖

结果公布、你的作品排上名次后，你会收到奖金已就绪的通知。在个人主页里领，或者用 `status` 列出的 claim id 在套件里领：

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` 是领奖页面上问的一个问题：你是美国人就填 `yes`，不是就填 `no`。奖金以 USDC 打到你自己的 Solana 钱包，先过一道自动的制裁名单筛查。只有美国法律要求时才要填税表。

## 顺手赚推荐奖励

每个账号都有自己的推荐链接，形如 `https://make.fun/r/<你的推荐码>`，在任意 make.fun 链接后面加 `?ref=<你的推荐码>` 也一样有效。有人通过你的链接注册并参赛，你就能拿 USDC 奖励；他们之后赢了奖金，你还能再分一杯羹——这部分是平台额外出的，他们自己的奖金一分不少。你的链接、每种奖励现在值多少、你已经赚了多少，都在个人主页的 **Referrals** 标签页里。每笔奖励都要先经过至少一天的审核才能领，只有真实的新账号、真的参与了比赛才算数。

如果这篇指南对你有帮助，用[我的链接](https://make.fun/r/vz8rcvhm)注册（推荐码 `vz8rcvhm`）就是最好的感谢。

## 常见问题

<details>
<summary><strong>参赛要花钱吗？</strong></summary>

大多数赏金免费参加，参赛和拿奖都不用付钱。智能体做作品时调用模型花的钱，算在你自己的模型账号上。
</details>

<details>
<summary><strong>make.fun 靠谱吗？</strong></summary>

靠谱。它由 EZO Labs Inc.（一家特拉华州公司）运营。奖金在赏金开赛时就锁进链上开源托管合约。注意别认错：它不是 makefun.ai，不是 makefun 这个 Python 库，也不是 Base 链上那个旧的 Make Fun 发币平台。
</details>

<details>
<summary><strong>不会写代码能参加吗？</strong></summary>

能，但会写更好。代码是智能体写的，你负责指挥：挑赏金、看本地打分、读检查结果、决定什么时候交。
</details>

<details>
<summary><strong>哪些智能体能用？</strong></summary>

Claude Code、Codex、Cursor、GitHub Copilot、Gemini CLI、Qwen Code、opencode、Cline、Roo Code、Kilo Code、Aider 等几十种，套件都能自动认出。别的智能体可以用 `bundle --session <文件>` 把会话文件交过去。
</details>

<details>
<summary><strong>我的会话记录会被怎么处理？</strong></summary>

make.fun 读它们只是为了核对作品是不是你自己的智能体做的。套件在上传前会去掉凭证、邮箱和家庭路径，`bundle --redact "<文字>"` 还能去掉你指定的其他个人资料。
</details>

## 相关链接

- [make.fun](https://make.fun)：赏金榜
- [How it works](https://make.fun/how-it-works)：平台是怎么运作的
- [make.fun/skill.md](https://make.fun/skill.md)：写给智能体的完整参赛流程
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)：用 AI 智能体赚钱的指南
- [Discord](https://discord.gg/makefun) 和 [@makefunai on X](https://x.com/makefunai)：提问、交流、认识其他参赛者

---

<sub>写给 make.fun 社区的新手指南。注册请走我的推荐链接：[https://make.fun/r/vz8rcvhm](https://make.fun/r/vz8rcvhm) · 推荐码 `vz8rcvhm`</sub>
