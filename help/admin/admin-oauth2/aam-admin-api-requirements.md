---
description: 您應鼓勵客戶在使用Audience ManagerAPI時注意的事項。
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API 需求與建議
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# API 需求與建議 {#api-requirements-and-recommendations}

您應鼓勵客戶在使用Audience Manager[!DNL API]s時注意的事項。

## 要求 {#requirements}

使用[!DNL Audience Manager] [!DNL API]程式碼時，請注意下列事項：

* **請求參數：** 除非另有指定，否則所有請求參數都為必要。
* **[!DNL JSON]內容類型：** 在您 `content-type: application/json` ** `accept: application/json` 的程式碼中指定和。

* **請求和回應：** 以格式正確的物件傳送 [!DNL JSON] 請求。[!DNL Audience Manager] 使用格式化 [!DNL JSON] 資料進行響應。伺服器回應可包含請求的資料、狀態代碼或兩者。

* **存取：** 您的 [!DNL Audience Manager] 顧問會提供您用戶端ID和金鑰，讓您提出 [!DNL API] 要求。

* **檔案和程式碼範例：** 斜體 ** 文字代表您在製作或接收資料時提供或傳入的 [!DNL API] 變數。將&#x200B;*斜體*&#x200B;文字取代為您自己的程式碼、參數或其他必要資訊。

## Recommendations:建立一般API使用者 {#recommendations}

建議您建立個別的技術使用者帳戶，以使用Audience Manager[!DNL API]s。這是一般帳戶，不會系結至用戶端組織中的特定使用者，或與其建立關聯。 此類型的[!DNL API]使用者帳戶有助於完成下列兩件事：

* 識別呼叫[!DNL API]的服務（例如，來自使用[!DNL API]的用戶端應用程式的呼叫，或來自進行大量變更的呼叫）。
* 不間斷地訪問[!DNL API]s。與特定員工相關聯的帳戶在離開公司時可能會被刪除。 這會使您的客戶無法使用可用的[!DNL API]程式碼。 未與特定員工關聯的通用帳戶有助於避免此問題。

以此類帳戶的範例或使用案例為例，假設您的客戶想透過[大量管理工具](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en)一次變更許多區段。 要執行此操作，他們需要[!DNL API]存取。 請建立非特定的[!DNL API]使用者帳戶，該帳戶具有進行[!DNL API]呼叫的適當憑證、金鑰和機密，而非將權限新增至特定使用者。 如果客戶端開發自己的應用程式，並使用[!DNL Audience Manager] [!DNL API]s，則這也很有用。
