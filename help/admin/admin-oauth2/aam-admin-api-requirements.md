---
description: 您應鼓勵客戶在使用Audience Manager API時注意的事項。
seo-description: 您應鼓勵客戶在使用Audience Manager API時注意的事項。
seo-title: API 需求與建議
title: API 需求與建議
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# API 需求與建議{#api-requirements-and-recommendations}

您應鼓勵客戶在使用Audience Manager [!DNL API]時注意的事項。

## 要求 {#requirements}

使用[!DNL Audience Manager] [!DNL API]代碼時，請注意以下事項：

* **請求參數：除** 非另有指定，否則所有請求參數都為必要參數。
* **[!DNL JSON]內容類型：** 指定 `content-type: application/json` ** `accept: application/json` 並在程式碼中。

* **請求和回應：以** 正確格式化的物件傳送 [!DNL JSON] 請求。[!DNL Audience Manager] 以格式化 [!DNL JSON] 資料回應。伺服器回應可包含要求的資料、狀態碼或兩者。

* **存取：** 您的 [!DNL Audience Manager] 顧問會提供您用戶端ID和金鑰，讓您提出 [!DNL API] 要求。

* **檔案和程式碼範例：** 斜體 ** 文字代表您在製作或接收資料時提供或傳入的 [!DNL API] 變數。以您自己的程式碼、參數或其他必要資訊取代&#x200B;*斜體*&#x200B;文字。

## 建議：建立一般API使用者{#recommendations}

我們建議建立個別的技術使用者帳戶，以搭配Audience Manager [!DNL API]使用。這是一般帳戶，不會系結至客戶組織中的特定使用者或與其關聯。 此類[!DNL API]使用者帳戶可協助完成下列2項工作：

* 識別呼叫[!DNL API]的服務（例如，來自使用[!DNL API]的用戶端應用程式的呼叫，或來自進行大量變更的呼叫）。
* 不間斷地訪問[!DNL API]。與特定員工關聯的帳戶在離開公司時可能會被刪除。 這會使客戶無法使用可用的[!DNL API]程式碼。 未系結至特定員工的一般帳戶有助於避免此問題。

舉例來說，假設您的客戶想要使用[批量管理工具](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)一次變更許多區段，這就是此類帳戶的使用案例。 若要這麼做，他們需要[!DNL API]存取權。 請建立非特定的[!DNL API]使用者帳戶，該帳戶具有適當的認證、金鑰和機密，以進行[!DNL API]呼叫，而不是新增權限給特定使用者。 如果客戶端開發自己使用[!DNL Audience Manager] [!DNL API]的應用程式，則此功能也很有用。
