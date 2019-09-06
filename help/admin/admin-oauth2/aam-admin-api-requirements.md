---
description: 當客戶使用Audience Manager API時，應鼓勵他們注意。
seo-description: 當客戶使用Audience Manager API時，應鼓勵他們注意。
seo-title: API需求和建議
title: API需求和建議
uuid: eda9cf92-f0 c8-4394-85522-0de9 e7 b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# API需求和建議 {#api-requirements-and-recommendations}

當客戶使用Audience Manager [!DNL API]時，應鼓勵他們注意。

## 要求 {#requirements}

使用 [!DNL Audience Manager][!DNL API] 程式碼時請注意下列事項：

* **請求參數：** 除非另行指定，否則需要所有請求參數。
* **[!DNL JSON]內容類型：** 指定 `content-type: application/json`*和*`accept: application/json` 在您的程式碼中。

* **要求與回應：** 將請求傳送為格式正確的 [!DNL JSON] 物件。[!DNL Audience Manager] 回應 [!DNL JSON] 格式資料。伺服器回應可以包含要求的資料、狀態代碼或兩者。

* **存取：**[!DNL Audience Manager] 您的顧問會提供客戶ID和金鑰，讓您 [!DNL API] 可以提出要求。

* **說明文件和程式碼範例：***斜體文字* 代表您在製作或接收 [!DNL API] 資料時提供或傳入的變數。使用您自己的程式碼、參數或其他必要資訊取代 *斜體* 文字。

## 建議：建立一般API使用者 {#recommendations}

建議您建立個別的技術使用者帳戶，以便使用Audience Manager [!DNL API]。這是一般帳戶，不會系結至客戶組織中的特定使用者或關聯。此 [!DNL API] 類型的使用者帳戶有助於完成兩項工作：

* 識別哪些服務正在呼叫(例如 [!DNL API] 來自客戶應用程式使用我們 [!DNL API]的s或進行大量變更的呼叫)。
* 不間斷地存取 [!DNL API]s.綁定給特定員工的帳戶在離開公司時可能會被刪除。這會使您的客戶無法使用可用 [!DNL API] 的程式碼。未系結至特定員工的一般帳戶有助於避免此問題。

作為此類型帳戶的範例或使用案例，假設您的客戶想要一次使用 [大量管理工具變更許多區段](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)。若要這麼做，他們需要 [!DNL API] 存取。不要新增權限給特定使用者，請建立非特定的 [!DNL API] 使用者帳戶，其中包含適當的憑證、索引鍵和秘密來 [!DNL API] 進行呼叫。如果客戶的開發應用程式使用 [!DNL Audience Manager][!DNL API]s.
