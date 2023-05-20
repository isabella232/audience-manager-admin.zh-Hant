---
description: 使用「Audience Manager管理」工具中的「伺服器」頁可以建立新的HTTP伺服器或編輯現有伺服器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: 建立或編輯 HTTP 伺服器
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 6%

---

# 建立或編輯 HTTP 伺服器 {#create-or-edit-an-http-server}

使用 [!UICONTROL Servers] 的子菜單。在Audience Manager管理工具中，可以建立新的HTTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須 [!UICONTROL DEXADMIN] 角色以建立新伺服器或編輯現有伺服器。

1. 要建立新伺服器，請轉到 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請按一下 **[!UICONTROL Label]** 的雙曲餘切值。
1. 指定此伺服器所需的標籤。
1. 從 **[!UICONTROL Protocol]** 下拉清單中，選擇所需的協定： [!DNL HTTP]。
1. 填寫欄位: 

   * **[!UICONTROL Domain]:** 為此伺服器指定所需的域（主機）。
   * **[!UICONTROL Port]:** 指定此伺服器所需的埠。 每個加密類型都顯示預設埠。 如有必要，可更改預設埠
   * **[!UICONTROL Maximum Users Per Request]:** 指定此伺服器允許的每個請求的最大用戶數。
   * **[!UICONTROL URL Prefix]:** 指定 [!DNL URL] 用於此伺服器的前置詞。
   * **[!UICONTROL Authentication URL]:** 指定 [!UICONTROL Authentication URL] 為 `HTTP` 伺服器。
   * **[!UICONTROL Authentication]:** 指定所需的身份驗證方法： **[!UICONTROL None]**。 **[!UICONTROL Username/Password]**&#x200B;或 **[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]:** 名稱 [!DNL HTTP] 由客戶提供的標題，其中包含 [!DNL HTTP] 簽名密鑰。 預設值為 [!UICONTROL X-Signature]，如下例所示：

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** 用於簽名的密鑰 [!DNL HTTP] 請求，由客戶提供。
   * **[!UICONTROL Show Signature Key]:** 切換是否在瀏覽器中顯示簽名。
   * **[!UICONTROL HTTP Signature Encryption Method]:** 指定用於加密簽名的方法。 使用 [!UICONTROL SHA1] 除非客戶另有選擇。

   >[!NOTE]
   >
   >如果要啟用 [用於即時資料傳輸的OAuth 2.0身份驗證](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en) 對於合作夥伴，請填寫下表中的欄位。 中的欄位 *斜體* 需要像桌子裡一樣填滿。

   | 名稱 | 值 |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *授權*] |
   | [!UICONTROL Password] | 您的密碼(_p) |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 按一下 **[!UICONTROL Create]** 如果要建立新伺服器，或按一下 **[!UICONTROL Update]** 編輯現有伺服器。
