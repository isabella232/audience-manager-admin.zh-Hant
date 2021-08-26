---
description: 使用「OAuth2用戶端」頁面，在您的Audience Manager設定中檢視OAuth2用戶端清單。 您可以編輯或刪除現有客戶端或建立新客戶端，前提是分配了適當的用戶角色。
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: OAuth2 用戶端
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# OAuth2 用戶端 {#oauth-clients}

使用[!UICONTROL OAuth2 Clients]頁可查看[!DNL Audience Manager]配置中的[!UICONTROL OAuth2]客戶端清單。 您可以編輯或刪除現有客戶端或建立新客戶端，前提是分配了適當的用戶角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>請確定您的Audience Manager閱讀「Analytics使用指南」中的[OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth)檔案。

[!DNL OAuth2] 是授權的開放標準，可代表資源擁有者提供對 [!DNL Audience Manager] 資源的安全委派存取。

![](assets/oauth.png)

您可以按一下所需欄的標題，以遞增或遞減順序排序每個欄。

使用[!UICONTROL Search]方塊或清單底部的分頁控制項，以尋找所需的用戶端。

## 建立或編輯OAuth2用戶端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience Manager[!UICONTROL Admin]工具中的[!UICONTROL OAuth2 Clients]頁可建立新的[!UICONTROL Oauth2]客戶端或編輯現有客戶端。

1. 要建立新的[!UICONTROL OAuth2]客戶端，請按一下「**[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**」。 要編輯現有的[!UICONTROL OAuth2]客戶端，請在&#x200B;**[!UICONTROL Client ID]**&#x200B;列中按一下所需的客戶端。
1. 為此[!UICONTROL OAuth2]客戶端指定所需的名稱。 請注意，這僅是記錄的名稱。
1. 指定[!UICONTROL OAuth2]用戶端的電子郵件地址。 一個電子郵件地址的限制。
1. 從&#x200B;**[!UICONTROL Partner]**&#x200B;下拉式清單中，選取所需的合作夥伴。
1. 在&#x200B;**[!UICONTROL Client ID]**&#x200B;方塊中，指定所需的ID。 這是提交[!DNL API]請求時使用的值。 在您從前一步驟的下拉式清單中選擇[!UICONTROL Partner]後，開始輸入時，首碼會自動填入。 正確格式為&lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>。
1. 視需要選取或取消選取&#x200B;**[!UICONTROL Restrict to Partner Users]**&#x200B;核取方塊。 如果選中此複選框，則用戶必須是為所選合作夥伴列出的[!DNL Audience Manager]用戶。 根據最佳實務，建議您選取此選項。
1. 在&#x200B;**[!UICONTROL Scope]**&#x200B;區段中，視需要選取或取消選取&#x200B;**[!UICONTROL Read]**&#x200B;和&#x200B;**[!UICONTROL Write]**&#x200B;核取方塊。
1. 在&#x200B;**[!UICONTROL Grant Type]**&#x200B;區段中，選取所需的授權方式。 建議您使用[!UICONTROL Password]和[!UICONTROL Refresh-token]選項的預設設定。

   * **[!UICONTROL Implicit]**:如果選取此選項，則 [!UICONTROL Redirect URI] 會啟用方塊。在驗證後，使用者會獲得自動存取權杖，並立即傳送至重新導向[!DNL URI]。
   * **[!UICONTROL Authorization Code]**:如果選取此選項，則 [!UICONTROL Redirect URI] 會啟用方塊。在驗證後，將用戶返回到客戶端，然後發送到重定向[!DNL URI]。
   * **[!UICONTROL Password]**:使用用戶輸入的密碼來驗證用戶，而不是通過授權伺服器自動驗證嘗試。
   * **[!UICONTROL Refresh_token]**:用於刷新已過期的訪問令牌一段長時間。

1. 在&#x200B;**[!UICONTROL Redirect URI]**&#x200B;方塊中，指定所需的[!DNL URI]。 只有在選擇&#x200B;**[!UICONTROL Implicit]**&#x200B;和&#x200B;**[!UICONTROL Authorization_code]**&#x200B;授予類型時，才啟用此選項。 **[!UICONTROL Redirect URI]**&#x200B;方塊可讓您指定可接受[!DNL URI]值的逗號分隔值。 這是在批准客戶端進行[!DNL API]訪問後，將客戶端的用戶重定向到的[!DNL URI]。
1. 指定存取和重新整理Token過期所需的過期時間（以秒為單位）。

   * **[!UICONTROL Access Token Expiration Time]**:存取權杖發出後有效的秒數。若要使用平台預設值（12小時），則可能為null。 也可以是–1，以指出存取權杖不會過期。
   * **[!UICONTROL Refresh Token Expiration Time]**:重新整理Token發出後有效的秒數。若要使用平台預設值（30天），則可能為null。

1. 按一下 **[!UICONTROL Save]**.

若要刪除[!UICONTROL OAuth2]客戶端，請按一下&#x200B;**[!UICONTROL OAuth2 Clients]**，然後按一下所需客戶端的&#x200B;**[!UICONTROL Actions]**&#x200B;列中的![](assets/icon_delete.png)。

>[!MORELIKETHIS]
>
>* [API 需求與建議](../admin-oauth2/aam-admin-api-requirements.md)

