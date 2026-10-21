# 介面急診室｜無障礙 UX 陪診師・梨安

「生成式 AI：文字與圖像」第七週獨立作業。與碩士論文無關；非W3C官方產品或符合性認證工具。

## 主要作品
- [RAG 02 Colab對話展示](https://colab.research.google.com/drive/1u89jRYeyD14_MZpqBu0KaM0BC7AaqbhI)
- [RAG 01 Colab建庫](https://colab.research.google.com/drive/1yH9OctfmIrS7CMhuKTRQGbJPa9DUjMXy)
- [rag-data.zip固定公開直連](https://raw.githubusercontent.com/50819just/week07-ui-accessibility-rag/acbef1fd4a1b0e5e21b292a46b4cfaf1b987f002/rag-data.zip)

助教可儲存RAG 02副本，以自己的Colab Secrets `Groq`由上至下執行，不須先執行第一份。公開Notebook不包含Key。連續API呼叫至少間隔65秒，避免免費方案速率限制。

## 知識來源
[WCAG 2.2固定Recommendation](https://www.w3.org/TR/2024/REC-WCAG22-20241212/)的18項成功準則＋4個詞彙定義。英文正文保留，中文別名與解說為非官方。Copyright © 2020-2024 World Wide Web Consortium；[文件授權](https://www.w3.org/copyright/document-license-2023/)。非完整規範，無W3C背書。

原始`source-documents.zip`和正式向量`rag-data.zip`不同；後者根目錄為index.faiss、documents.json、index_doc_ids.json、config.json。

## 架構與來源
沿用[老師Notebook](https://github.com/yenlung/Generative-AI) commit `f424ee3ed3c909830d7df08d17491dacacf88b61`，固定六套件、EmbeddingGemma 2、FAISS、AIsuite／Groq指定模型。AI協助資料整理、公開下載、原創Prompt、別名輔助排序、Gradio、引用檢查與測試，沒有冒稱本人獨立撰寫。修改格見程式修改對照。

## 展示邊界
來源分數不是正確率；原文片語與引用ID驗證不代表中文語意必然正確。公開Gradio會使用啟動者Groq額度，不要輸入機密；展示後在第18節將STOP_DEMO設True停止。連結臨時有效，Colab才是可重現入口。
