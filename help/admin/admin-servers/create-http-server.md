---
description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的HTTP伺服器或編輯現有伺服器。
seo-description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的HTTP伺服器或編輯現有伺服器。
seo-title: 建立或編輯 HTTP 伺服器
title: 建立或編輯 HTTP 伺服器
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: d518ba4011f203a7d450ce76d8c1924f7d73a815
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 7%

---


# 建立或編輯 HTTP 伺服器{#create-or-edit-an-http-server}

使用Audience Manager管理工具中的[!UICONTROL Servers]頁面建立新的HTTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具有[!UICONTROL DEXADMIN]角色，才能建立新伺服器或編輯現有伺服器。

1. 要建立新伺服器，請轉至&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請在&#x200B;**[!UICONTROL Label]**&#x200B;列中按一下所需的伺服器。
1. 指定此伺服器的所需標籤。
1. 從&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉式清單中，選取所需的通訊協定：[!DNL HTTP]。
1. 填寫欄位: 

   * **[!UICONTROL Domain]：指** 定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]：指** 定此伺服器的所需埠。每個加密類型都會顯示預設埠。 如有必要，您可以更改預設埠
   * **[!UICONTROL Maximum Users Per Request]：指** 定此伺服器允許的每個請求使用者人數上限。
   * **[!UICONTROL URL Prefix]：指** 定要 [!DNL URL] 用於此伺服器的前置詞。
   * **[!UICONTROL Authentication URL]:** 指定 [!UICONTROL Authentication URL] 此服 `HTTP` 務器。
   * **[!UICONTROL Authentication]：指** 定所需的驗證方法： **[!UICONTROL None]**、 **[!UICONTROL Username/Password]**&#x200B;或 **[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]:** 由客戶提 [!DNL HTTP] 供的包含簽名密鑰的標 [!DNL HTTP] 頭名稱。預設值為[!UICONTROL X-Signature]，如下例所示：

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

   * **[!UICONTROL HTTP Signature Key]:** 客戶提供用來簽署 [!DNL HTTP] 請求的金鑰。
   * **[!UICONTROL Show Signature Key]:** 切換是否在瀏覽器中顯示簽名。
   * **[!UICONTROL HTTP Signature Encryption Method]:** 指定加密簽名的方法。請使用[!UICONTROL SHA1]，除非客戶另有選擇。

   >[!NOTE]
   >
   >如果您想要為合作夥伴啟用[OAuth 2.0即時資料傳輸](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html)驗證，請填入下表中的欄位。 *斜體字*&#x200B;中的欄位必須完全填入表格中。

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

1. 如果要建立新伺服器，請按一下&#x200B;**[!UICONTROL Create]** ，如果要編輯現有伺服器，請按一下&#x200B;**[!UICONTROL Update]**。
