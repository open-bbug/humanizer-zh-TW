# humanizer-zh-TW (AI 文字潤飾工具)

這是一份 AI 工具的 Agent Skill，旨在辨識並消除由 AI 生成的文字痕跡，讓文句讀起來更自然、更像真人撰寫。

本工具的規則基於維基百科的「[AI 寫作特徵](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)」綜合指南，並針對台灣繁體中文的用語習慣進行了在地化調整。

## 安裝說明

### 方法一：透過 npx 一鍵安裝（推薦）

```bash
npx skills add https://github.com/open-bbug/humanizer-zh-TW.git
```

這是最簡單的安裝方式，會自動將技能安裝到正確的目錄。

### 方法二：透過 Git 安裝

#### claude 範例

```bash
# 將 Humanizer-zh-TW 安裝到 skills 目錄
git clone https://github.com/open-bbug/humanizer-zh-TW.git ~/.claude/skills/humanizer-zh-TW
```

#### gemini 範例

```bash
# 將 Humanizer-zh-TW 安裝到 skills 目錄
git clone https://github.com/open-bbug/humanizer-zh-TW.git ~/.gemini/skills/humanizer-zh-TW
```

#### codex 範例

```bash
# 將 Humanizer-zh-TW 安裝到 skills 目錄
git clone https://github.com/open-bbug/humanizer-zh-TW.git ~/.codex/skills/humanizer-zh-TW
```

### 方法三：手動安裝

要使用此技能，請將 `SKILL.md` 文件放置在您的 Agent 的技能目錄中。

例如，建立一個名為 `humanizer-zh-TW` 的資料夾，並將 `SKILL.md` 放入其中：

```bash
<your_skills_directory>/humanizer-zh-TW/SKILL.md
```

Agent 啟動時將會讀取此技能，並在適當的時機啟用。

## 使用說明

當您需要編輯或校對一段由 AI 生成的文字時，可以直接向 Agent 下達指令，要求其「人性化」該段內容。Agent 會自動運用此技能來分析並改寫您的文章。

**Claude Code 範例：**

重啟 Claude Code 或重新載入 skills 後，在對話中輸入：

```bash
/humanizer-zh-TW 請幫我潤飾以下文案
/humanizer-zh-TW 請幫我潤飾 xxx 文件內容
```

**範例提示：**

> 「請幫我校對這篇文章，讓它讀起來更自然，消除 AI 的寫作痕跡。」

### 改寫範例

**改寫前 (AI 味很重)：**
> 新的軟體更新作為公司致力於創新的證明。此外，它提供了無縫、直觀和強大的用戶體驗——確保用戶能夠高效地完成目標。這不僅僅是一次更新，更是我們思考生產力方式的革命。產業專家認為這將對整個產業產生持久影響，彰顯了公司在不斷演變的技術版圖中的關鍵作用。

**改寫後 (人性化)：**
> 這次的軟體更新加入了批次處理、鍵盤快速鍵和離線模式。來自測試用戶的早期回饋相當正面，大多數人表示任務完成的速度變快了。

## 主要功能特色

此技能會偵測並修正以下常見的 AI 寫作模式：

* **過度強調意義**：誇大事件的歷史地位或象徵意義。
* **宣傳式口吻**：使用過多華麗、不中立的形容詞。
* **膚淺的分析**：使用分詞短語來營造虛假的深度。
* **模糊的來源**：將論點歸因於「專家認為」、「報告顯示」等模糊群體。
* **公式化結構**：例如「挑戰與未來展望」等樣板式段落。
* **AI 常用詞彙**：過度使用「此外」、「至關重要」、「深入探討」等詞語。
* **結構僵化**：濫用三段論、破折號或表情符號。
* **對話痕跡**：遺留下「希望這對您有幫助」等與聊天機器人的對話內容。

## 常見 AI 詞彙列表

以下詞彙在 AI 文件中出現頻率很高：

* 此外、至關重要、深入探討、強調
* 持久的、增強、培養、獲得
* 突出、相互作用、複雜/複雜性
* 格局（抽象名詞）、關鍵性的、展示
* 織錦（抽象名詞）、證明、強調
* 寶貴的、充滿活力的

### 中文語境特殊性

在翻譯和適配過程中，我們考慮了中文寫作的特點：

* 某些英文寫作模式在中文中表現不同（如標題大小寫問題）
* 增加了適合中文語境的提示詞
* 調整了部分表達方式以符合中文使用習慣
* 增加了繁體中文的範例

## 貢獻

若發現翻譯問題或想要改進文件，歡迎提交 Issue 或 Pull Request。

## 參考資料

本技能指南主要基於 [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) 頁面，由 WikiProject AI Cleanup 社群維護。

## 支持

如果 `go-ccstatusline` 節省了您的時間或讓您的 Claude Code 會話變得更加愉快，請考慮請我喝杯咖啡。每一項貢獻都有助於維持專案的積極維護。

<a href='https://ko-fi.com/O4O21YCECP' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

## 許可

本翻譯專案遵循原專案的許可協議，核心內容基於維基百科社群的觀察和總結。
