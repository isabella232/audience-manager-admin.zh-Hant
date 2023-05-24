---
description: 使用「Audience Manager管理員」工具中的「伺服器」頁面，建立新的HTTP伺服器或編輯現有的伺服器。
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

使用 [!UICONTROL Servers] 頁面，以建立新的HTTP伺服器或編輯現有的伺服器。Audience Manager管理工具。

>[!NOTE]
>
>您必須擁有 [!UICONTROL DEXADMIN] 角色，以建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請前往 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 若要編輯現有伺服器，請在 **[!UICONTROL Label]** 欄。
1. 指定此伺服器的所需標籤。
1. 從 **[!UICONTROL Protocol]** 下拉式清單，選取所需的通訊協定： [!DNL HTTP].
1. 填寫欄位: 

   * **[!UICONTROL Domain]：** 指定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]：** 指定此伺服器的所需連線埠。 每個加密型別都會顯示預設連線埠。 您可以視需要變更預設連線埠
   * **[!UICONTROL Maximum Users Per Request]：** 指定此伺服器允許的每個請求的最大使用者數。
   * **[!UICONTROL URL Prefix]：** 指定 [!DNL URL] 用於此伺服器的前置詞。
   * **[!UICONTROL Authentication URL]：** 指定 [!UICONTROL Authentication URL] 針對此 `HTTP` 伺服器。
   * **[!UICONTROL Authentication]：** 指定所需的驗證方法： **[!UICONTROL None]**， **[!UICONTROL Username/Password]**，或 **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]：** 的名稱 [!DNL HTTP] 由客戶提供的標題，其中包含 [!DNL HTTP] 簽章金鑰。 預設值為 [!UICONTROL X-Signature]，如下列範例所示：

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

   * **[!UICONTROL HTTP Signature Key]：** 用來簽署 [!DNL HTTP] 要求，由客戶提供。
   * **[!UICONTROL Show Signature Key]：** 切換是否要在瀏覽器中顯示簽名。
   * **[!UICONTROL HTTP Signature Encryption Method]：** 指定我們用來加密簽名的方法。 使用 [!UICONTROL SHA1] 除非客戶另有偏好。

   >[!NOTE]
   >
   >如果您想要啟用 [用於即時資料傳輸的OAuth 2.0驗證](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en) 若是合作夥伴，請填寫下表中的欄位。 中的欄位 *斜體* 需要完全依照表格中的方式填寫。

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
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 按一下 **[!UICONTROL Create]** 如果您要建立新伺服器，或按一下 **[!UICONTROL Update]** 如果您正在編輯現有伺服器。
