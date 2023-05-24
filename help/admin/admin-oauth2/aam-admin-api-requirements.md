---
description: 建議客戶在使用Audience ManagerAPI時注意的事項。
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

您應鼓勵客戶在使用Audience Manager時注意的事項 [!DNL API]s.

## 要求 {#requirements}

使用時，請注意下列事項 [!DNL Audience Manager] [!DNL API] 程式碼：

* **要求引數：** 除非另有指定，否則所有要求引數都是必要的。
* **[!DNL JSON]內容型別：** 指定 `content-type: application/json` *和* `accept: application/json` 在您的程式碼中。

* **要求與回應：** 以正確格式化的形式傳送請求 [!DNL JSON] 物件。 [!DNL Audience Manager] 回應 [!DNL JSON] 格式化資料。 伺服器回應可包含要求的資料、狀態代碼或兩者。

* **存取：** 您的 [!DNL Audience Manager] 顧問將為您提供使用者端ID和金鑰，讓您建立 [!DNL API] 要求。

* **檔案和程式碼範例：** 文字輸入 *斜體* 代表您在進行或接收時提供或傳入的變數 [!DNL API] 資料。 Replace *斜體* 包含您自己的程式碼、引數或其他必要資訊的文字。

## Recommendations：建立通用API使用者 {#recommendations}

建議您建立個別的技術使用者帳戶來使用Audience Manager [!DNL API]s.這是一般帳戶，與您使用者端組織內的特定使用者沒有關係或沒有關聯。 此型別 [!DNL API] 使用者帳戶有助於完成2件事：

* 識別呼叫的服務 [!DNL API] (例如，從使用我們的應用程式的使用者端應用程式呼叫 [!DNL API]或進行大量變更時)。
* 提供對的不中斷存取 [!DNL API]s.與特定員工繫結的帳戶可能會在員工離開公司時刪除。 這會導致您的客戶無法使用可用的 [!DNL API] 程式碼。 未與特定員工繫結的一般帳戶有助於避免此問題。

作為此類帳戶的範例或使用案例，假設您的客戶希望使用一次變更許多區段 [大量管理工具](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). 為此，他們需要 [!DNL API] 存取。 與其將許可權新增至特定使用者，不如建立非特定、 [!DNL API] 具有適當認證、金鑰和密碼的使用者帳戶 [!DNL API] 呼叫。 如果使用者端開發自己的應用程式，且這些應用程式使用 [!DNL Audience Manager] [!DNL API]s.
