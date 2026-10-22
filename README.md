# 介面急診室｜無障礙 UX 陪診師・梨安

「生成式 AI：文字與圖像」第七週獨立課程作業，不使用碩士論文資料。非W3C官方產品或符合性認證工具。

## 三步開始
1. 開啟 **[RAG 02 Colab](https://colab.research.google.com/drive/1u89jRYeyD14_MZpqBu0KaM0BC7AaqbhI)**，儲存自己的副本，在Colab Secrets設定自己的 `Groq`，允許該副本存取。
2. 按「全部執行」，等待安裝、知識庫驗證與模型載入。
3. 開第17節Gradio網址，直接問介面問題。不必先跑RAG 01，也不必每次先跑三題模型測試。

`RUN_SAMPLE_ANSWER=False`、`RUN_ANSWER_TESTS=False`為正常展示預設；批次生成只在需要回歸時開啟。實際問答、截圖與限制見[QA總結](QA總結.md)，操作排錯見[指南](使用與繳交指南.md)。

## 主題白話說明
WCAG是「網頁內容無障礙指引」，可理解為讓更多人能看懂、操作網站的設計參考。使用者說出介面問題，梨安先查文件再回答；查不到就不亂猜，來源可以展開核對。展示重點是RAG，不是規範背誦。

## 知識庫與模型
- [RAG 01：建立知識庫](https://colab.research.google.com/drive/1yH9OctfmIrS7CMhuKTRQGbJPa9DUjMXy)
- [rag-data.zip固定公開直連](https://raw.githubusercontent.com/50819just/week07-ui-accessibility-rag/acbef1fd4a1b0e5e21b292a46b4cfaf1b987f002/rag-data.zip)
- 資料：WCAG 2.2固定版本18項成功準則＋4項詞彙定義，共22份TXT。
- 流程：TXT → EmbeddingGemma 2 → FAISS四檔ZIP → 新問題檢索 → AIsuite／Groq `openai/gpt-oss-120b` → Gradio及原文核對。
- 保留[老師Notebook](https://github.com/yenlung/Generative-AI)固定六套件及必要架構，基準commit `f424ee3ed3c909830d7df08d17491dacacf88b61`。

原文包是source-documents.zip；正式rag-data.zip根目錄為index.faiss、documents.json、index_doc_ids.json、config.json，不能互換。

## 資料權利與協作
來源：[W3C WCAG 2.2，2024-12-12 Recommendation](https://www.w3.org/TR/2024/REC-WCAG22-20241212/)。Copyright © 2020-2024 World Wide Web Consortium；[文件授權](https://www.w3.org/copyright/document-license-2023/)。英文正文保留；中文別名與解說非官方，非完整規範，無W3C背書。

AI協助資料整理、程式、人設Prompt、介面與QA，不冒稱本人已獨立撰寫。見[AI協作說明](AI協作與本人理解說明.md)、[System Prompt](梨安_System_Prompt.txt)及[逐格修改對照](程式修改對照.md)。

## 使用界線
引用ID與英文片語存在，不代表中文解釋全對；相似度不是正確率。有限22份節錄不能取代實際網站檢測。

連續生成可能等待約65秒，修復或429重試會再增加時間。公開Gradio使用啟動者額度，不輸入個資或機密；第18節將STOP_DEMO設True可停止。臨時展示不是永久網站，正式入口為Colab，其他人重新執行須使用自己的Key。
