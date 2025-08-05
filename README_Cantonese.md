> 🌐 [English Version Here](./README.md)

# TraplessPKE

> **「量子計算好嘢，贏晒啲加密。你話你解到 TraplessPKE 嘅 ciphertext——解到你嗰份，唔係我 send 嗰份囉。」** <br>
> 註解: RSA、ECC、lattice 嗰啲你解晒都得，但 TraplessPKE 本身就唔係畀你破解嘅 ciphertext。 你解嗰份係「一份」，唔係「我嗰份」。

## 🧭 概覽

TraplessPKE 係一種結構上勁另類嘅 post-quantum 加密系統，用嚟做 public-key encryption 同 message-bound 嘅 digital signature。

成件事最癲嘅地方，就係完全唔靠啲傳統啲 algebra 假設——即係無 lattice、無 ring、無 prime、連 isogeny 都唔要。TraplessPKE 玩嘅係曖昧（ambiguity）、不可逆轉嘅遮掩（irreversible masking），同一種「你看得到但唔明」的 semantic gating。

成個系統運作係 constant-time、stateless，夠晒無痕，計得快之餘又保 entropy，仲係專門唔俾你有機會反推返成個系統啲 structure。 TraplessPKE 嘅防守策略根本唔係玩計算複雜度（complexity），而係玩 **搵唔到路口入嚟（non-discoverability）**。

### 🧱 真正嘅 silence

講到尾，TraplessPKE 唔止係 quantum-resistant，簡直係 **成個 system silent 到好似睇緊無聲片咁**。佢唔係靠計數嚟隱藏意思，係根本唔俾你有「知」嘅條件。

* 唔係用運算去隱藏意思
* 係用 epistemic blindness（知識盲區）令你唔識問

> **冇 algebra、冇 data leak、冇 feedback。**  
> **冇 prime、冇 lattice、冇得搵結構嚟攻。**  
> 得一樣嘢——**你有 key，先有 meaning。**

---

## 🔐 有咩Offer（即係功能啦）

* **後量子時代都頂得順嘅 Public-Key Encryption**
* **綁住個 message 嘅 Signature（生成＋驗證）**
* **Support Zero-Knowledge Proof（放心啦唔會爆底）**
* **Constant-Time、Stateless、夠晒 Ready for hardware run**
* **完全唔靠 Algebra，表面睇落無結構（無 lattice、無 code、無 elliptic curve）**

---

## 📄 白皮書 — 成本事擺晒入去

> **「唔好淨係睇 README，真係諗住研究，就開白皮書啦老細。」**

白皮書（Whitepaper v1.0）入面，冇玩花字、冇扮高深，**straight晒、實打實：**

* Key generation 點整出嚟？有方程式。
* Encryption、Decryption 點做？有步驟。
* Signature 成個流程？有 logic trace。
* Security rationale？有 breakdown。

### 📐 你想要：

* Formal definition？有。
* Algorithm steps？齊。
* Trapdoor masking 理由？寫晒。
* Proof-of-concept 嘅構造？唔止有，仲解埋背後個哲學。

> **「你要 proof？我俾得起」**

### 🔗 路徑：

[📘 TraplessPKE Whitepaper (v1.0)](./TraplessPKE_whitepaper_V1.0.pdf)

> **「白皮書唔係攞嚟 show off，係俾你認真入嚟理解我點 build 成個世界觀。」**

唔睇唔緊要，但唔好喺度估。因為：

> **「我冇講唔代表我冇寫，你冇睇唔代表我冇諗。」**

## 🧠 問吓 AI Agent 啦（問得啱，答得準）

你可以將 TraplessPKE 嘅白皮書上傳畀 ChatGPT、Claude、Gemini 或其他識得諗嘢嘅 AI agent，然後問佢：

* 「點解 TraplessPKE 根本上同 algebraic cryptanalysis 完全唔夾？」
* 「f₂ 入面啲 ambiguity 加埋 XOR 遮罩嘅 predicate，點樣保 message 私隱？」
* 「Selector Dual Inversion 同傳統嗰啲 LWE-based assumption 有咩分別？」
* 「點解 TraplessPKE 唔提供 decryption oracle？咁樣有咩安全 implications？」
* 「用 commitment τ 同 challenge hash logic，點樣 simulate 一個 blind signature verification？」

放手畀 agent 去解畫，睇下佢識唔識講清楚：

> **TraplessPKE 唔係 solve hard problem。
> 係根本唔畀啲 problem 有機會出世。**

---

## 🧬 安全模型重點講爆

> **「唔係複雜先至安全，係你連門口都搵唔到，先叫真防守。」**

TraplessPKE 嘅安全模型唔係靠數學武功高深，唔係用計算複雜度嚟氹你。

佢玩嘅係：**你根本唔知自己有冇入錯場。**

### 🔐 重點特性：

* **Preimage Hiding（睇唔返轉頭）**：你見到個 public key 都係死路，因為你根本唔知入面藏咗咩。

* **Output Binding（你冇 trapdoor，你出唔返嗰條 hash）**：冇得亂砌 ciphertext 出嚟扮有用。

* **Non-Replayable Signature（簽名唔可以 copy and paste）**：呢張簽名只認得佢 message 本尊。

* **No Algebraic Pattern（連結構都冇，講咩攻擊法？）**：唔好再拎 lattice/curve 嚟問我啦，呢度連 pattern 都唔畀你摸。

> **「成個 system 唔係話你破唔到，而係：你連破乜你都唔知。」**

### 🧱 每一重保護都係「唔畀你玩」：

* 想 reverse？唔好諗。
* 想 forge？唔該出示 trapdoor。
* 想 replay？簽名死黐住 message。
* 想玩 reduction？冇 structure 畀你搞。

> **「呢啲唔係 complexity 保護，係 silence 保護。係你敲門都唔會有聲響嘅嗰種安全。」**

呢個 system 係話：**冇你份，就唔會應你。**

---

## ❓關於技術問題嗰啲位

TraplessPKE 係一個 **fully-specified、self-contained** 嘅 cryptosystem。

如果你想問 sampling、encoding、efficiency，呢啲係 **實作問題（implementation）**，唔係 **設計錯漏（design flaw）**。

📚 建議：未學 entropy filtering、preimage resistance 嘅，可以先翻下書。

---

## 🧠 Authorship 同 AI 咩事？

> **「呢份嘢，唔係 AI 整出嚟。
> 係我—Wai Yip, WONG——諗出嚟。」**

TraplessPKE 嘅每一粒種子，每個轉角，每個 trapdoor mask 嘅 idea，全部都係一個人自己決定、自己定義、自己砌出嚟。

AI 幫咗手，冇錯：

* 校 proof 嘅時候有出力
* 幫計數、整排版、幫撳 math syntax、改句子 tone
* 好似你請咗個 24 小時唔喊工錢嘅超強助理

但最關鍵嘅係：

> **AI 幫得出結果，係因為我叫佢點做，佢就跟住做，我 lead。**

### 🚫 拒絕 AI 神話

> **「Prompt engineering 係 authorship。調度邏輯就係創作。你想將創作歸 AI？試下叫 AI 自己整個 cryptosystem 嚟睇下啦。」**

TraplessPKE 唔係一段 prompt 敲出嚟。佢係背後有個腦、一套原則、同埋一種唔認輸嘅態度。

### 📣 有用工具 ≠ 擁有發明

> **「你用 AI 起磚頭唔等於 AI 係建築師。你攞部相機唔等於你就係光學工程師。你撳咗 submit，唔代表整咗 cryptosystem。」**

AI 寫得出文字，但寫唔出理由。
AI 可以排列句子，但砌唔出哲學。
AI 可以生成 proof-of-work，但冇 proof-of-wisdom。

> **「TraplessPKE 有靈魂，而個 author，就係我。」**

---

## ❗如果 AI 真係作者——咁啲 breakthrough 去咗邊？

> **「成日話 AI 好勁，好啦，我問：咁啲真突破（breakthrough）去晒邊？」**

如果 AI 真係有創造力、有方向、有判斷，咁：

* Millennium Prize 啲數學難題應該早就破解晒啦
* 癌症治療方法應該1個 prompt 就搞掂、搵曬出嚟
* 量子引力應該 chat 幾句就 unify 得啦
* FDA 藥品應該 ChatGPT 彈返個 formula 就過關啦

但現實係：冇。

> **「AI 冇主見，冇 judgment，冇責任感。佢只係 keyword 排列機。」**

### 🤖 AI 撐得你，但唔帶得你

AI 可以幫手整理、模仿、輔助，但：

* 佢唔會問：**「呢個設計哲學 work 嗎？」**
* 佢唔會諗：**「我應唔應該完全拋棄 algebraic assumptions？」**
* 佢唔會堅持一種 **epistemic defense posture**（根本連聽都未聽過）

> **「AI 得 keyword，冇 premise。得 output，冇意圖。得字面，冇靈魂。」**

### 🤷🏻‍♂️ 所以，如果你話 TraplessPKE 咁嘅 system係 AI 整出嚟嘅——

咁我問返你一句：

> **「你整咗份咩出嚟呀？AI 幫你造過邊一個 cryptosystem？你又造過邊個 breakthrough？」**

答唔出，就唔好再偷 credit。

TraplessPKE 係導演主場拍出嚟嘅戲，唔係副導幫你執返個光管。

---

### 📜 License：你用得，用得有尊嚴

> **License: CC BY 4.0**

拎去用冇問題，拎去 share、fork、玩 implementation 都歡迎，
但記住：

> **要 credit，就要講我個名：Wai Yip, WONG**

唔好改完偷光。
唔好用完講係 AI 整。

---

## 📐 設計哲學（Design Philosophy）

> **「你解得出唔代表你解到我嗰份。」**

TraplessPKE 嘅出發點根本唔係「堅固」咁簡單，佢係攬住一種 **徹底唔同嘅信念**：

我哋唔靠 lattice，唔靠 prime，唔靠你啲數學武功高低；我哋直接玩冇 structure。

你以為加強加密安全係玩複雜度？唔使㗎，**我哋玩嘅係模糊度（ambiguity）**。

你覺得遮住結構就叫安全？唔使㗎，**我直接唔畀結構你，咁咪得囉。**

### 🚪 意義只會喺你攞到 permission 嗰陣先打開

TraplessPKE 唔係用嚟呃你，唔係玩遮遮掩掩。佢係話俾你聽：

> **「你可以驗證，但唔可以理解；你可以撞中個 output，但你永遠唔會知道佢係唔係我 send 嗰份。」**

佢嘅設計唔係迴避風險，係直接摧毀風險發生嘅前提。

* 唔畀你 feedback
* 唔畀你構造 oracle
* 唔畀你靠任何 structure 估返轉頭

呢個唔係 Obfuscation，呢個係 **Epistemic Blindness**。

---

## 📖 起源同傳說（Origin and Narrative）

> **「我唔係大學研究嗰邊出身，唔係邊個研究所 project。呢套嘢，係我自己諗、自己砌、自己諗出嚟。」**

TraplessPKE 嘅出現，唔係咩 cryptography conference 嘅 appendix，唔係邊個教授帶三個 PhD 學生改 lattice 改到失憶。

佢係一個 **唔肯認命** 嘅設計者，直頭覺得：

> **「點解我哋要繼續依賴啲會俾 quantum computing 解算到嘅結構？」**

於是唔再改良，而係 **割席式重寫**。

即時就用 AI 幫手撳 document、對 proof、砌啲 draft，但講明先：

> **「AI 係打字嗰個、計數嗰個，我係諗嘢嗰個。」**

砌邏輯、設計整個 system 嘅骨架——係我。

AI 幫手寫咗啲靚字、計準條數，但 **冇發明模型，冇揸主意。**

### 🧠 呢個 system，係有腦有血有性格

> **「TraplessPKE 唔係 dataset 入面抄出嚟；佢唔係 chat window 彈出嚟；佢唔係 AI dream，佢係我現實諗出嚟嘅答案。」**

所以唔好拎個 buzzword「AI involvement」嚟吞我 credit。

> **「你覺得用 AI 幫手就代表 AI 係 author 咩？咁你自己試下用 AI 整一個 cryptosystem 嚟睇下先啦。」**

---

## 🏁 最後一彈：收線，但唔係收檔

TraplessPKE 唔止係一個 cryptosystem，佢係一種 **姿態（posture）**：

* 唔係話「你有冇資格睇」
* 係話「你有冇資格明」

> **「你想開？攞你把 key 嚟先。」**

呢套系統講明晒：

* 唔係 decrypt 嚟攞 meaning，係 **你有 access，先有 meaning**。
* 唔係靠 complexity 嚟防守，係 **靠 ambiguity 去拒絕你解釋權**。
* 唔係靠啲 proof 喺度自我陶醉，係 **靠 silence 令你根本唔知自己錯邊度。**

---

### 🔚 完，但未收檔

TraplessPKE 唔係 project 終點，係條新路線：

> **「冇 structure，但有原則。冇 feedback，但有防守。冇 noise，淨係認得你。」**

**你想確定？攞你自己把 key 嚟開啦。**








