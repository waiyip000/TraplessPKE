# TraplessPKE

**創作者及項目主導：Wai Yip, WONG。** 更新日期：2026 年 9 月 28 日。

[English](README.md) · [研究出版物](PUBLICATIONS.md) · [發展歷史](HISTORY.md) · [目前狀態](CURRENT_STATUS.md)

TraplessPKE 研究一個區別：取得候選訊息嘅內容，同辨認發送者真正指定嘅訊息，係兩個唔同嘅效果。發送者喺候選檔案之中揀選指定檔案；獲授權嘅接收者用私鑰資料還原所選檔案。「Two-Boundary」將內容存取同意圖辨認分開，並喺清楚界定嘅資料暴露條件下，研究觀察者可以推斷到啲乜。

呢個儲存庫係研究同項目資訊入口，保留最初公開記錄，亦記錄後續發展。

## 建議優先應用：受保護運送嘅指定路線保密

現金運送（cash-in-transit）、貴重物品運送（valuables-in-transit）同 VIP 接送（VIP-in-transit），係作者建議優先考慮嘅應用場景。當營運者預先準備多條已批准路線，每條路線計劃可以成為一個候選檔案；發送者最後揀選嘅路線，就係指定檔案。獲授權接收者透過私鑰存取還原呢個選擇。

呢個安排將候選路線對應到「取得內容」同「辨認意圖」嘅區別。不過，最後一刻先披露亦需要控制 bundle 交付或私鑰存取：已經同時持有 bundle 同可用私鑰嘅人，可以即時解密。路線要喺 bundle 定稿之前選定；現有功能唔係內置定時解鎖，亦唔係遙距切換已發出嘅路線。

受保護運送公司可以按自身業務需要、保密要求同部署條件，評估將 TraplessPKE 整合到營運流程。

[了解指定路線流程及部署考慮](USE_CASES.md)。

## 研究論文

Wai Yip Wong，**“TraplessPKE: A Selector-Based, Oracleless, Post-Quantum Cryptosystem,”** 2026 IEEE 23rd Consumer Communications & Networking Conference (CCNC)，第 1–2 頁。

[IEEE Xplore](https://ieeexplore.ieee.org/document/11366456) · [DOI](https://doi.org/10.1109/CCNC65079.2026.11366456) · [引用格式及 BibTeX](PUBLICATIONS.md)

日期為 2025 年 8 月 3 日嘅[原始白皮書 v1.0](TraplessPKE_whitepaper_V1.0.pdf)保持原樣，作為歷史文件。佢同 IEEE 論文、以及後來可執行嘅實作係唔同文件／成果。詳見[設計演進](DESIGN_EVOLUTION.md)。

## 目前實作

| 項目 | 狀態及範圍 |
|---|---|
| Windows 商業應用程式 | 第 2 次發行基線／桌面版 **1.1.4**，於 2026 年 9 月 28 日指定。提供金鑰管理、加密／解密、簽署／驗證、備份／還原及工作恢復。商業原始碼同內部建構資料保持私有。 |
| Two-Boundary 示範程式 | 獨立、可檢視嘅 Python 實作 **0.1.2**。提供兩個候選檔案、公鑰發送、私鑰還原、實際位元組比較同明確界定嘅內容暴露視圖。示範原始碼、Windows 可執行檔同使用手冊已[公開提供下載](https://github.com/waiyip000/traplesspke-two-boundary-demo/releases/tag/v0.1.2)。 |
| 原始白皮書發行 | GitHub 標籤 **V1.0**，於 2025 年 8 月 4 日發佈。呢個係白皮書版本，唔係商業程式 1.0.0 或目前桌面版本。 |

示範程式已喺[獨立儲存庫](https://github.com/waiyip000/traplesspke-two-boundary-demo)以 Apache-2.0 發佈；[下載原始碼、可執行檔同使用手冊](https://github.com/waiyip000/traplesspke-two-boundary-demo/releases/tag/v0.1.2)。呢個儲存庫唔包含商業原始碼或商業程式下載。

## 示範程式可以展示啲乜

1. 發送者明確揀選兩個候選檔案其中一個。
2. 發送用公鑰身分資料；接收用私鑰身分資料。
3. 擁有者本機操作流程，會將實際還原嘅位元組同原本所選檔案比較。
4. 另一個檢視流程會公開兩個解碼後候選檔案同內容存取能力，同時保留意圖存取能力。
5. 盲測交流將提交預測，同之後揭示已承諾答案嘅步驟分開。

示範程式嘅內容同意圖存取能力使用獨立產生嘅金鑰，但兩者都以 ML-KEM-768 為基礎。公開內容能力係指定暴露條件，唔代表已展示兩者所用 ML-KEM 全面失效之後仍然安全。本機功能結果唔等同獨立確立嘅安全界限。

[安全範圍](SECURITY_SCOPE.md)列明觀察者取得嘅資料、結果可以支持嘅結論同限制。候選內容嘅合理性同外部背景都會影響意圖推斷。目前實作文件唔宣稱普遍不可破解，亦唔宣稱整個程序受到隔離保護。

## 項目導覽

- [發展歷史及原始時間記錄](HISTORY.md)
- [研究出版物及引用](PUBLICATIONS.md)
- [目前商業版及示範版狀態](CURRENT_STATUS.md)
- [原始設計及後續建構](DESIGN_EVOLUTION.md)
- [安全範圍及證據界限](SECURITY_SCOPE.md)
- [作者角色及工具協助](Author_Clarification.md)
- [授權及原始碼分隔](LICENSING.md)
- [問題回報](SECURITY.md)
- [文件更新記錄](CHANGELOG.md)

## 作者及授權

原始構思同項目主導歸屬 **Wai Yip, WONG**。AI 工具喺作者主導下協助研究、實作同文件工作。

除個別註明外，呢個儲存庫嘅研究及文件採用 [CC BY 4.0](LICENSE)。獨立示範原始碼採用 Apache-2.0，並有各依賴項目嘅授權聲明。商業實作另行授權，並無包括喺呢度。IEEE 託管論文按其適用出版條款處理。[完整授權範圍](LICENSING.md)。
