---
description: 使用「OAuth2用戶端」頁面，在Audience Manager設定中檢視OAuth2用戶端清單。 您可以編輯或刪除現有客戶機或建立新客戶機，前提是您已分配了適當的用戶角色。
seo-description: 使用「OAuth2用戶端」頁面，在Audience Manager設定中檢視OAuth2用戶端清單。 您可以編輯或刪除現有客戶機或建立新客戶機，前提是您已分配了適當的用戶角色。
seo-title: OAuth2 用戶端
title: OAuth2 用戶端
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 2%

---


# OAuth2 用戶端 {#oauth-clients}

使用[!UICONTROL OAuth2 Clients]頁可查看[!DNL Audience Manager]配置中的[!UICONTROL OAuth2]客戶機清單。 您可以編輯或刪除現有客戶機或建立新客戶機，前提是您已分配了適當的用戶角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>請確定您的客戶閱讀Audience Manager使用指南中的[OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth)檔案。

[!DNL OAuth2] 是授權的開放標準，代表資源擁有者提供對資 [!DNL Audience Manager] 源的安全委託存取。

![](assets/oauth.png)

您可以按一下所需欄的標題，以遞增或遞減順序來排序每個欄。

使用[!UICONTROL Search]方塊或清單底部的編頁控制項，以尋找所需的用戶端。

## 建立或編輯OAuth2用戶端{#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience Manager [!UICONTROL Admin]工具中的[!UICONTROL OAuth2 Clients]頁面建立新的[!UICONTROL Oauth2]用戶端或編輯現有用戶端。

1. 要建立新的[!UICONTROL OAuth2]客戶端，請按一下&#x200B;**[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**。 要編輯現有的[!UICONTROL OAuth2]客戶機，請在&#x200B;**[!UICONTROL Client ID]**&#x200B;列中按一下所需的客戶機。
1. 指定此[!UICONTROL OAuth2]客戶端的所需名稱。 請注意，這僅是記錄的名稱。
1. 指定[!UICONTROL OAuth2]客戶端的電子郵件地址。 電子郵件地址的限制。
1. 從&#x200B;**[!UICONTROL Partner]**&#x200B;下拉式清單中，選擇所要的合作夥伴。
1. 在&#x200B;**[!UICONTROL Client ID]**&#x200B;方塊中，指定所要的ID。 這是提交[!DNL API]請求時使用的值。 在您從前一步驟的下拉式清單中選擇[!UICONTROL Partner]後，開始輸入時，首碼會自動填入。 正確的格式為&lt; *`partner subdomain`* - *`Audience Manager username`*。
1. 視需要選取或取消選取&#x200B;**[!UICONTROL Restrict to Partner Users]**&#x200B;核取方塊。 如果選中此複選框，則用戶必須是為所選夥伴列出的[!DNL Audience Manager]用戶。 建議您選取此選項作為最佳實務。
1. 在&#x200B;**[!UICONTROL Scope]**&#x200B;區段中，視需要選取或取消選取&#x200B;**[!UICONTROL Read]**&#x200B;和&#x200B;**[!UICONTROL Write]**&#x200B;核取方塊。
1. 在&#x200B;**[!UICONTROL Grant Type]**&#x200B;區段中，選擇所需的授權方式。 建議您使用[!UICONTROL Password]和[!UICONTROL Refresh-token]選項的預設設定。

   * **[!UICONTROL Implicit]**:如果您選取此選項，則 [!UICONTROL Redirect URI] 會啟用方塊。在經過驗證後，使用者會獲得自動存取Token，並立即傳送至重新導向[!DNL URI]。
   * **[!UICONTROL Authorization Code]**:如果您選取此選項，則 [!UICONTROL Redirect URI] 會啟用方塊。在經過驗證後，用戶將返回到客戶端，然後被發送到重定向[!DNL URI]。
   * **[!UICONTROL Password]**:使用用戶輸入的密碼來驗證用戶，而不是通過授權伺服器自動驗證嘗試。
   * **[!UICONTROL Refresh_token]**:用於在較長的時間內刷新過期的訪問令牌。

1. 在&#x200B;**[!UICONTROL Redirect URI]**&#x200B;方塊中，指定所要的[!DNL URI]。 僅當選擇&#x200B;**[!UICONTROL Implicit]**&#x200B;和&#x200B;**[!UICONTROL Authorization_code]**&#x200B;授權類型時，才啟用此選項。 **[!UICONTROL Redirect URI]**&#x200B;方塊可讓您指定可接受[!DNL URI]值的逗號分隔值。 這是在批准客戶端進行[!DNL API]訪問後，將客戶端的[!DNL URI]用戶重定向到的。
1. 指定存取和重新整理Token過期所需的過期時間（以秒為單位）。

   * **[!UICONTROL Access Token Expiration Time]**:存取Token在發出後有效的秒數。使用平台預設值時可能為null（12小時）。 也可以是-1，以指出存取Token不會過期。
   * **[!UICONTROL Refresh Token Expiration Time]**:重新整理Token發出後有效的秒數。使用平台預設值（30天）時可能為null。

1. 按一下 **[!UICONTROL Save]**.

要刪除[!UICONTROL OAuth2]客戶端，請按一下&#x200B;**[!UICONTROL OAuth2 Clients]** ，然後按一下&#x200B;**[!UICONTROL Actions]**&#x200B;列中![](assets/icon_delete.png)以查找所需的客戶端。

>[!MORELIKETHIS]
>
>* [API 需求與建議](../admin-oauth2/aam-admin-api-requirements.md)

