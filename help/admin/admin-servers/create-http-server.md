---
description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的HTTP伺服器或編輯現有伺服器。
seo-description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的HTTP伺服器或編輯現有伺服器。
seo-title: 建立或編輯 HTTP 伺服器
title: 建立或編輯 HTTP 伺服器
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 7%

---


# 建立或編輯 HTTP 伺服器{#create-or-edit-an-http-server}

使用 [!UICONTROL Servers] Audience Manager管理工具中的頁面來建立新的HTTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具有角色 [!UICONTROL DEXADMIN] 才能建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請前往 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請在列中按一下所需的服 **[!UICONTROL Label]** 務器。
1. 指定此伺服器的所需標籤。
1. 從下拉 **[!UICONTROL Protocol]** 式清單中，選擇所要的通訊協定： [!DNL HTTP].
1. 填寫欄位: 

   * **[!UICONTROL Domain]:**指定此伺服器所需的網域（主機）。
   * **[!UICONTROL Port]:**為此伺服器指定所需的埠。 每個加密類型都會顯示預設埠。 如有必要，您可以更改預設埠
   * **[!UICONTROL Maximum Users Per Request]:**指定此伺服器允許的每個請求使用者人數上限。
   * **[!UICONTROL URL Prefix]:**指定要[!DNL URL]用於此伺服器的前置詞。
   * **[!UICONTROL Authentication URL]:**指定此[!UICONTROL Authentication URL]伺服器的`HTTP`名稱。
   * **[!UICONTROL Authentication]:**指定所需的驗證方法：**[!UICONTROL None]**、**[!UICONTROL Username/Password]**或&#x200B;**[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]:**由客戶提[!DNL HTTP]供的包含簽名密鑰的標[!DNL HTTP]頭名稱。 預設值為[!UICONTROL X-Signature]，如下例所示：

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

   * **[!UICONTROL HTTP Signature Key]:**用於簽署請求的金[!DNL HTTP]鑰，由客戶提供。
   * **[!UICONTROL Show Signature Key]:**切換是否在瀏覽器中顯示簽名。
   * **[!UICONTROL HTTP Signature Encryption Method]:**指定我們用來加密簽名的方法。 除非客[!UICONTROL SHA1]戶另有選擇，否則請使用。

   >[!NOTE]
   >
   >如果您想要為合作夥伴啟 [用OAuth 2.0驗證，以便即時傳輸資料](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) ，請填入下表中的欄位。 斜體字 *中的欄* ，必須完全填入表格中。

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
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 如果 **[!UICONTROL Create]** 要建立新伺服器，請按一下，或者如果 **[!UICONTROL Update]** 要編輯現有伺服器，請按一下。