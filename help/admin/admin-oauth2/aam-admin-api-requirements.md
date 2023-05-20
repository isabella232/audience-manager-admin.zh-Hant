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

您應鼓勵客戶在與Audience Manager合作時注意的事項 [!DNL API]s

## 要求 {#requirements}

使用時請注意以下事項 [!DNL Audience Manager] [!DNL API] 代碼：

* **請求參數：** 除非另有指定，否則所有請求參數都是必需的。
* **[!DNL JSON]內容類型：** 指定 `content-type: application/json` *和* `accept: application/json` 你的密碼。

* **請求和響應：** 以格式正確的方式發送請求 [!DNL JSON] 的雙曲餘切值。 [!DNL Audience Manager] 響應 [!DNL JSON] 格式化資料。 伺服器響應可以包含請求的資料、狀態代碼或兩者。

* **訪問：** 您 [!DNL Audience Manager] 顧問將為您提供客戶端ID和密鑰，以便您 [!DNL API] 請求。

* **文檔和代碼示例：** 文本 *斜體* 表示在生成或接收時提供或傳遞的變數 [!DNL API] 資料。 替換 *斜體* 包含您自己的代碼、參數或其他必需資訊的文本。

## Recommendations:建立通用API用戶 {#recommendations}

我們建議建立一個單獨的技術用戶帳戶以使用Audience Manager [!DNL API]s這是一個普通帳戶，它不與客戶機組織中的特定用戶關聯或關聯。 此類型 [!DNL API] 用戶帳戶可幫助完成兩項任務：

* 確定呼叫的服務 [!DNL API] (例如，來自使用我們 [!DNL API]或進行批量更改)。
* 提供對 [!DNL API]s與特定員工關聯的帳戶在離開公司時可以刪除。 這將阻止您的客戶使用可用 [!DNL API] 代碼。 不與特定員工關聯的通用帳戶有助於避免此問題。

作為此類型帳戶的示例或使用案例，假設客戶希望同時使用 [批量管理工具](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en)。 要做到這一點，他們需要 [!DNL API] 訪問。 不是向特定用戶添加權限，而是建立非特定用戶， [!DNL API] 具有相應憑據、密鑰和機密的用戶帳戶 [!DNL API] 呼叫。 如果客戶開發使用 [!DNL Audience Manager] [!DNL API]s
