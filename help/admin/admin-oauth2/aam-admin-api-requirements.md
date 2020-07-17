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

您應鼓勵客戶在使用Audience Manager時注意的事 [!DNL API]項。

## 要求 {#requirements}

使用程式碼時，請注意 [!DNL Audience Manager] 下 [!DNL API] 列：

* **請求參數：** 除非另有指定，否則所有請求參數都是必要的。
* **[!DNL JSON]內容類型：**在程`content-type: application/json`式碼&#x200B;*中指*`accept: application/json`定和指定。

* **要求與回應：** 以格式正確的物件傳送 [!DNL JSON] 請求。 [!DNL Audience Manager] 以格式化資 [!DNL JSON] 料回應。 伺服器回應可包含要求的資料、狀態碼或兩者。

* **存取：** 您的 [!DNL Audience Manager] 顧問會提供您用戶端ID和金鑰，讓您提出 [!DNL API] 要求。

* **檔案和程式碼範例：** 斜體 *文字* ，代表您在製作或接收資料時提供或傳入的變 [!DNL API] 數。 以您 *自己的程式碼* 、參數或其他必要資訊取代斜體文字。

## 建議： 建立一般API使用者 {#recommendations}

我們建議建立個別的技術使用者帳戶，以搭配Audience Manager [!DNL API]使用。 這是一般帳戶，不會系結至客戶組織中的特定使用者或與其關聯。 此類使用者帳 [!DNL API] 戶可協助完成下列2項工作：

* 識別呼叫的服務( [!DNL API] 例如，來自使用我們的用戶端應用程式的呼叫， [!DNL API]或進行大量變更的呼叫)。
* 不間斷地存取 [!DNL API]s。 與特定員工關聯的帳戶在離開公司時可能會被刪除。 這會使客戶無法使用可用的程 [!DNL API] 式碼。 未系結至特定員工的一般帳戶有助於避免此問題。

舉例來說，假設您的客戶想要使用大量管理工具一次變更許多區段，就是此類帳戶的使 [用案例](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)。 為此，他們需要存 [!DNL API] 取。 請建立非特定的使用者帳戶，該帳戶具有適當的認證、金鑰 [!DNL API] 和密碼，以進行呼叫，而不是新增權限至特定 [!DNL API] 使用者。 如果用戶端開發使用s的應用程式，這個功能也會很有 [!DNL Audience Manager][!DNL API]用。
