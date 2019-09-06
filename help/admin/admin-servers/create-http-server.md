---
description: 使用Audience Manager管理工具中的「伺服器」頁面建立新的HTTP伺服器或編輯現有伺服器。
seo-description: 使用Audience Manager管理工具中的「伺服器」頁面建立新的HTTP伺服器或編輯現有伺服器。
seo-title: 建立或編輯HTTP伺服器
title: 建立或編輯HTTP伺服器
uuid: 1ef0e751-e239-4dc6-a4 f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 建立或編輯HTTP伺服器 {#create-or-edit-an-http-server}

使用Audience Manager管理工具中的 [!UICONTROL Servers] 頁面建立新的HTTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具備此 [!UICONTROL DEXADMIN] 角色才能建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請前往 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**。若要編輯現有的伺服器，請按一下 **[!UICONTROL Label]** 欄中所要的伺服器。
1. 指定此伺服器所要的標籤。
1. 從 **[!UICONTROL Protocol]** 下拉式清單中，選取所需的通訊協定： [!DNL HTTP]。
1. 填寫欄位: 

   * **[!UICONTROL Domain]：** 指定此伺服器的所需網域(主機)。
   * **[!UICONTROL Port]：** 指定此伺服器所要的連接埠。會針對每個加密類型顯示預設連接埠。您可視需要變更預設連接埠
   * **[!UICONTROL Maximum Users Per Request]：** 指定此伺服器允許每個請求的使用者數目上限。
   * **[!UICONTROL URL Prefix]：** 指定用於此伺服器的 [!DNL URL] 首碼。
   * **[!UICONTROL Authentication URL]：** 指定此 [!UICONTROL Authentication URL]`HTTP` 伺服器的。
   * **[!UICONTROL Authentication]：** 指定所要的驗證方法： **[!UICONTROL None]****[!UICONTROL Username/Password]****[!UICONTROL SSH Key]**&#x200B;或。
   * **[!UICONTROL HTTP Signature Header]：** 客戶提供 [!DNL HTTP] 的標題名稱，包含 [!DNL HTTP] 簽名金鑰。預設值如下 [!UICONTROL X-Signature]所示：

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

   * **[!UICONTROL HTTP Signature Key]：** 客戶提供 [!DNL HTTP] 要求的索引鍵。
   * **[!UICONTROL Show Signature Key]：** 切換是否在瀏覽器中顯示簽名。
   * **[!UICONTROL HTTP Signature Encryption Method]：** 指定用來加密簽名的方法。除非客戶事先偏好，否則使用 [!UICONTROL SHA1] 。
   >[!NOTE]
   >
   >如果您想要啓用 [OAuth2.0驗證，以便為合作夥伴即時傳送](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) 資料，請填寫下表中的欄位。*斜體* 格式的欄位必須填入表格中。

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
   | [!UICONTROL Username] | [!UICONTROL *授權&#x200B;*] |
   | [!UICONTROL Password] | your_ password_ here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 如果 **[!UICONTROL Create]** 您要建立新伺服器，請按一下， **[!UICONTROL Update]** 如果您正在編輯現有伺服器。