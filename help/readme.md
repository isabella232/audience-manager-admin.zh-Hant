---
source-git-commit: b76aa4a35a5216aabd60d07352a7c4bd2b3e6e32
translation-type: tm+mt

---
# 說明

**注意：此頁面(或任何讀我. md頁面)將不會發佈至客戶對應文件**

## 目錄目錄

+ `TOC.md` goot of the user guide provides the topic of the tries that are contained in the guide for this solution.
+ 每個使用手冊都有其專屬 `TOC.md`，您可以視需要訂購所有頁面/主題。
+ 所有使用者指南的第一頁都是 `overview.md`。

## 使用者指引

+ 使用者指南簡介稱為 `overview.md`
+ 使用者指南中的每個主題都有專屬的目錄。
   + 如果指南中有名為 *「實施」*&#x200B;的主題，對應的目錄就是 `/implementation`
+ 所有影像資產都會儲存在 `/assets` 使用者指南的根目錄中。
   + `/assets` 目錄中的所有影像都會本地化。
   + `/no-localize` 目錄中的任何影像都不會本土化(讓人意外！)。這可用來確保loc版本中的特定資產不必要重現。

## 使用者指南層級中繼資料

+ 描述使用手冊的中繼資料會儲存 `TOC.md`在此中。其中包括:
   + 產品-產品/功能名稱。
   + 雲端-此產品所屬的雲端。
   + 對象-目標指南的對象或原型。
   + 使用者指南-使用者指南名稱。

## 頁面層級中繼資料

+ 描述文件所需的中繼資料會儲存為每個頁面的一部分。其中包括:
   + title-頁面標題。
   + description- page說明。
   + seo-title- seo替代標題。
   + seo-description-用於SEO用途的替代標題。
   + short-title-(選用欄位)。
   + 索引-是/否-頁面會由Adobe的搜尋平台索引。
   + 翻譯-是/否-此頁面將會本地化。
   + 版本(主要用於AEM和Campaign)，以標示產品版本。
   + private-feature-package-主要用於AEM。
   + beta版-此產品是否為測試版？
   + 重新導向-可用來建立必要的參考至新頁面。
   + doc-type：參考(預設)/疑難排解/開發人員/教學課程/kb/白皮書。

## 更多資訊

如需更多發佈指示、樣式指南、範例和其他資源，請造訪 [協作文件回購](https://git.corp.adobe.com/AdobeDocs/collaborative-doc-instructions)
