# Feature 长文写作指南（第一卷 · Layer C）

> 目标：3800–4500 词英文研究长文，UCAS written work 候选。
> 暂拟题（三选一，第 7 周前定稿）：
> A. *Modular Arithmetic at War: How Counting Beat Hiding, from Baghdad to Your Browser*
> B. *The Trust Problem: Mathematics, Secrecy, and the HTTPS Padlock*
> C. 直译建议题：*How Modular Arithmetic Won the Second World War and Protects Your Browser*（面试场景可用，但学术上 A/B 更像研究论文而非科普）

---

## 一、先想清楚：这不是一篇编年史

主线「频率分析 → 恩尼格玛 → 图灵 → RSA → TLS」如果只按时间写，会变成《码书》摘要。Feature 必须有一个**贯穿的论点（thesis）**，五个节点只是论据。建议论点：

> **密码史是一场「对手的算力」与「数学难度」之间的军备竞赛：每一方都把己方的秘密转移到对方算不动的地方——先是转移统计规律（频率），再转移密钥空间（转子机），再转移计算问题本身（RSA），最后工程化地同时使用三者（TLS）。**

这样每一节回答同一个问题的一个版本：
- 频率分析：信息的**统计结构**在泄漏（语言有冗余）；
- 恩尼格玛：用机械把泄漏的统计结构**抹平**，把安全押在 10²⁰ 密钥空间上；
- 图灵：不硬算 10²⁰，用**人的操作失误**（crib）把搜索压成机械可满足性问题；
- RSA：**换赛道**——不再藏方法，而是公开方法、把秘密藏进「分解大数有多难」；
- TLS：承认没有一劳永逸，用**混合协议**把三种思想各用在刀刃上。

研究问题（Introduction 第一句就要给出）：
> *How did one algebraic structure — arithmetic modulo n — move from a Babylonian counting trick to the object that decides whether your bank transfer is safe?*

结论要回扣：数学难度是一种**工程材料**，和钢材一样有强度上限（量子计算 → 后量子密码），所以「谁赢」永远只是暂时的——这也自然引出帝国理工面试官最爱的开放问题。

## 二、逐节结构与字数（总计 ~4200 词）

| 节 | 内容 | 词数 | 数学框（boxed example） | 周次 |
|----|------|------|------------------------|------|
| §1 Introduction | 钩子 + 研究问题 + 路线图 + 论点 | 350 | 无 | 7 |
| §2 Language leaks: frequency analysis | 金迪、玛丽女王；「破译=统计推断」 | 600 | 频率表 + 一段移位密文手解 | 7 |
| §3 Enigma: the bet on key space | 转子机、plugboard、反射器自反性弱点 | 700 | 密钥空间计数（26³ × 环 × plugboard ≈ 1.5×10²⁰，注明教学简化） | 9 |
| §4 Turing: searching without brute force | 波兰人的置换论 → bombe = 约束排除机 | 800 | crib 排除示意（用第 8 周「人肉炸弹机」数据） | 9 |
| §5 RSA: hiding inside a hard problem | 密钥分发难题 → DH 握手 → 分解困难性 | 800 | p=23, g=5 握手 + p=3,q=11 加解密（复用 B3 已验算数字） | 10 |
| §6 TLS: the everyday compromise | 混合加密 + 证书 = 三千年思想的工程打包 | 450 | 时序图（引用 V 的 B4 配图） | 10 |
| §7 Conclusion | 回答 RQ + 量子展望 + 「军备竞赛」收束 | 250 | 无 | 10 |
| References | ≥18 条 | — | — | 12 |

写法要点：
1. **每节先写「核心段」**：主题句就是论点在本节的具体化（例：§5 核心段首句 "By 1975 the oldest problem in cryptography was no longer breaking ciphers but delivering keys."），先攒 7 个核心段给导师看，通过后再扩写——比从头顺写到 2000 词再推倒高效得多。
2. **数学框的纪律**：全文只允许 5 个 boxed example（即 §2–§6 各一），框外零公式；框内必须完整可验算。数字全部复用 `../../weekly-plan.md` 第四节已验算的例题，不要另编。
3. **每节结尾一句「军备递棒」**：显式写「X 解决了 Y 的泄漏，但制造了新泄漏 Z」，五节缝成一条线。这是审稿人和面试官会记住的结构。

## 三、范文：§1 开头 150 词（定调用，主编可仿写）

> The padlock on your bank's login page is 2,000 years old. Not the padlock — the idea behind it: that safety can live in a *secret agreement* rather than a hidden wall. When a ninth-century scholar in Baghdad read a intercepted letter by counting its letters, he proved something unsettling: messages leak the statistics of the language that made them. Every system in this essay is a response to that discovery. Enigma tried to machine away the statistics; Turing's bombe tried to exploit the humans operating it; RSA abandoned hiding the method altogether and hid the secret inside a problem whose answer takes longer than the age of the universe to compute...

（注意示范的三个技巧：物件钩子（锁）→ 一句话史论 → 全文路线图压进一段。）

## 四、史实红线（第 14 周核查逐条销号）

1. **考文垂神话**：不得写「丘吉尔为了保密放任考文垂被炸」。按 Hinsley 结论：Ultra 情报需平均使用、多数预警受多重因素限制；引用 Hinsley 卷 1 页码。
2. **图灵不是孤胆英雄**：必须给波兰三人组（Rejewski 的置换论是 bombe 的前提）和 U-110 缴获各至少一段；「bombe 是机电搜索器，不是计算机」要明写——这是流行文化错得最离谱的一点。
3. **凯撒「移 3 格」是文艺复兴转述**（苏维托尼乌斯只说字母转置）——范文已示范，Feature §2 引用时保持同样辨析口径。
4. **RSA 作者身份**：写 "Rivest, Shamir and Adleman"，首次出现可加 "(the initials give the name)"；同时注明 Clifford Cocks 1973 年已在 GCHQ 内部发明过同类方案（1997 年解密曝光）——这个「发明却没被允许公开」的细节是全文「方法 vs 秘密」论点的最佳注脚，强烈建议进 §5。
5. **TLS 数字**：现行 TLS 1.3 与 RSA-2048 的表述只引用 RFC 8446 与 NIST 页面，不引用博客。
6. 所有军事细节（Primrose、U-110、日期）对照资料卡⑦，人名舰名拼写逐一核对。

## 五、与 16 周计划的对接（主编时间表）

- **第 3–6 周（攒料期）**：不做写作，只做两件事——① 每周把 8 篇短文中可复用的叙事素材摘进 `Feature/materials.md`；② 精读《码书》对应章节时直接按本指南第二节在书页上做「论点标签」（哪段属于 §几）。
- **第 7 周交 §1–2**：注意是「核心段先行的 §1–2」，不是完整节。
- **第 9 周交 §3–4**：把第 8 周「人肉炸弹机」游戏的排除数据写进 §4 的框。
- **第 10 周交 §5–7 + 全文通读**：T 的 P3/P4 摘译此时正好完成，Feature 的引用与摘译互相比对，防止两处口径不一。
- **第 12 周导师反馈**：带 150 词 abstract 去（abstract 写法：RQ 一句 + 方法/结构一句 + 五节点各一词 + 结论一句）。
- **第 11、13–16 周**：与刊物流程合并，Feature 单独成 PDF 附老师说明信，归档备申请。

## 六、面试准备包（写完顺手做，1 页即可）

论文答辩式追问三题 + 2 分钟口头答案要点：
1. 「RSA 到底难在哪？给我讲讲为什么 2048 位够安全。」——答：不是「算不出」，是「已知最快算法（数域筛）的指数级复杂度 × 物理时间」；诚实说「我们不知道 P vs NP，也不保证没有新算法」——承认不确定性比背结论更加分。
2. 「图灵算不算发明了计算机？」——答：区分 bombe（专用搜索器）与 1936 论文的通用机（可计算性另属微积分卷话题）；这题就是考你是否分清流行叙事与史实。
3. 「如果量子计算机成熟，你的论文论点哪里会塌？」——答：论点不塌（军备竞赛逻辑正是预言了这次迭代），塌的是 §5 的「难度材料」：Shor 算法把分解降为多项式 → 后量子密码（格密码）换一种难度材料。收尾展示你读过 2024 年 NIST 后量子标准发布这件事即可。

## 七、参考文献起步清单（≥18 条的骨架）

一手文献（本地已有）：Diffie & Hellman 1976；Rivest/Shamir/Adleman 1978；Suetonius（Holland 公版英译）。
学术/权威二手：Singh《码书》；Hinsley《British Intelligence in the Second World War》vol.1；Hodges《Alan Turing: The Enigma》；Kozaczuk《Enigma》；Sale（Bletchley 重建 bombes 的技术报告，★官网可下）；RFC 8446；NIST FIPS 203/204/205（后量子标准）。
其余用 Google Scholar 顺藤：搜 "Rejewski permutation Enigma"、"bombe constraint satisfaction"、"Shannon redundancy cryptography"（把 §2 的「语言冗余」接到香农，正好为概率卷埋互引）。
引用格式：全文统一 Chicago 脚注（本刊既定脚注制，保持一致）。
