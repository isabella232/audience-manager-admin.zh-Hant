---
description: 您可以在「OAuth2從屬端」頁面，檢視Audience Manager組態中的OAuth2從屬端清單。 您可以編輯或刪除現有使用者端或建立新使用者端，前提是您已指派適當的使用者角色。
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

使用 [!UICONTROL OAuth2 Clients] 要檢視清單的頁面 [!UICONTROL OAuth2] 您的中的客戶 [!DNL Audience Manager] 設定。 您可以編輯或刪除現有使用者端或建立新使用者端，前提是您已指派適當的使用者角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>確保您的客戶閱讀 [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) 說明檔案(在Audience Manager使用手冊中)。

[!DNL OAuth2] 是授權向提供安全委派存取權的開放標準 [!DNL Audience Manager] 代表資源擁有者的資源。

![](assets/oauth.png)

您可以按一下所需欄的標頭，以遞增或遞減順序排序每個欄。

使用 [!UICONTROL Search] 方塊或清單底部的分頁控制項來尋找所需的使用者端。

## 建立或編輯OAuth2使用者端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用 [!UICONTROL OAuth2 Clients] Audience Manager中的頁面 [!UICONTROL Admin] 建立新工具 [!UICONTROL Oauth2] 使用者端或編輯現有使用者端。

1. 若要建立新的 [!UICONTROL OAuth2] 使用者端，按一下 **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. 若要編輯現有的 [!UICONTROL OAuth2] 使用者端，按一下 **[!UICONTROL Client ID]** 欄。
1. 為此指定所需的名稱 [!UICONTROL OAuth2] 使用者端。 請注意，這是僅記錄的名稱。
1. 指定 [!UICONTROL OAuth2] 使用者端的電子郵件地址。 電子郵件地址數不得超過1個。
1. 從 **[!UICONTROL Partner]** 從下拉式清單中，選取所需的合作夥伴。
1. 在 **[!UICONTROL Client ID]** 方塊中，指定所需的ID。 這是提交時使用的值 [!DNL API] 要求。 在您選擇後開始輸入時，前置詞會自動填入 [!UICONTROL Partner] 從上一步驟的下拉式清單中選取。 正確的格式為&lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. 選取或取消選取 **[!UICONTROL Restrict to Partner Users]** 核取方塊。 如果選取此核取方塊，使用者必須是 [!DNL Audience Manager] 為選取的合作夥伴列出的使用者。 最佳實務建議您選取此選項。
1. 在 **[!UICONTROL Scope]** 部分，選取或取消選取 **[!UICONTROL Read]** 和 **[!UICONTROL Write]** 核取方塊。
1. 在 **[!UICONTROL Grant Type]** 區段，選取所需的授權方式。 我們建議您使用 [!UICONTROL Password] 和 [!UICONTROL Refresh-token] 選項。

   * **[!UICONTROL Implicit]**：如果您選取此選項，系統就會將 [!UICONTROL Redirect URI] 方塊已啟用。 使用者在驗證後會獲得自動存取權杖，並會立即傳送到重新導向 [!DNL URI].
   * **[!UICONTROL Authorization Code]**：如果您選取此選項，系統就會將 [!UICONTROL Redirect URI] 方塊已啟用。 使用者在驗證後會傳回至使用者端，然後傳送至重新導向 [!DNL URI].
   * **[!UICONTROL Password]**：使用者是以使用者輸入的密碼進行驗證，而非透過授權伺服器來嘗試自動驗證。
   * **[!UICONTROL Refresh_token]**：用於重新整理過期的存取Token很長一段時間。

1. 在 **[!UICONTROL Redirect URI]** 方塊中，指定想要的 [!DNL URI]. 只有當您選取 **[!UICONTROL Implicit]** 和 **[!UICONTROL Authorization_code]** 授予型別。 此 **[!UICONTROL Redirect URI]** 方塊可讓您指定可接受的逗號分隔值 [!DNL URI] 值。 這是 [!DNL URI] 核准使用者端後，使用者端的使用者會重新導向至 [!DNL API] 存取。
1. 指定存取和重新整理權杖到期所需的到期時間（以秒為單位）。

   * **[!UICONTROL Access Token Expiration Time]**：存取權杖簽發後有效的秒數。 可以為空值以使用平台預設值（12小時）。 也可以是–1，表示存取權杖未過期。
   * **[!UICONTROL Refresh Token Expiration Time]**：重新整理權杖發出後有效的秒數。 若使用平台預設值（30天），則可以為空值。

1. 按一下 **[!UICONTROL Save]**.

若要刪除 [!UICONTROL OAuth2] 使用者端，按一下 **[!UICONTROL OAuth2 Clients]**，然後按一下  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 欄中尋找所需的使用者端。

>[!MORELIKETHIS]
>
>* [API 需求與建議](../admin-oauth2/aam-admin-api-requirements.md)

