---
description: 使用「OAuth客戶」頁面，在您的Audience Manager組態中檢視OAuth用戶端清單。您可以編輯或刪除現有用戶端，或建立新用戶端，前提是您已指派適當的使用者角色。
seo-description: 使用「OAuth客戶」頁面，在您的Audience Manager組態中檢視OAuth用戶端清單。您可以編輯或刪除現有用戶端，或建立新用戶端，前提是您已指派適當的使用者角色。
seo-title: OAuth Clients
title: OAuth Clients
uuid: 3e654053-fb2 f-4d8 f-a53 c-b5 c3 b8 dbdaaa
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# OAuth Clients {#oauth-clients}

使用 [!UICONTROL OAuth2 Clients] 頁面來檢視您設定 [!UICONTROL OAuth2] 中的客戶 [!DNL Audience Manager] 清單。您可以編輯或刪除現有用戶端，或建立新用戶端，前提是您已指派適當的使用者角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>確定您的客戶 [](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) 在[！DNL Audience Manager使用指南。

[!DNL OAuth2] 是開放標準，可代表資源擁有者提供安全委派存取 [!DNL Audience Manager] 資源。

![](assets/oauth.png)

您可以按一下所要的欄標題，以遞增或遞減順序排序每欄。

使用 [!UICONTROL Search] 方塊底部或清單底部的分頁控制項來尋找所需的用戶端。

## 建立或編輯OAuth用戶端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience [!UICONTROL OAuth2 Clients] Manager [!UICONTROL Admin] 工具中的頁面建立新 [!UICONTROL Oauth2] 用戶端或編輯現有用戶端。

1. 若要建立新 [!UICONTROL OAuth2] 客戶，請按一下 **[!UICONTROL OAuth2 Clients]** &gt; **[!UICONTROL Add OAuth2 Client]**。若要編輯現有 [!UICONTROL OAuth2] 用戶端，請按一下 **[!UICONTROL Client ID]** 欄中所要的用戶端。
1. 指定此 [!UICONTROL OAuth2] 用戶端所要的名稱。請注意，這是記錄的名稱。
1. 指定 [!UICONTROL OAuth2] 用戶端的電子郵件地址。電子郵件地址有限制。
1. 從 **[!UICONTROL Partner]** 下拉式清單中選擇所需的合作夥伴。
1. 在 **[!UICONTROL Client ID]** 方塊中指定所要的ID。這是提交 [!DNL API] 請求時使用的值。前置詞自動填入時，當您在上一步驟中的下拉式清單 [!UICONTROL Partner] 中選擇一個下拉式清單後，就會自動填入。正確格式為&lt; *`partner subdomain`*&gt;-&lt; *`Audience Manager username`*&gt;。
1. 視需要選擇或取消選取 **[!UICONTROL Restrict to Partner Users]** 核取方塊。如果選取此核取方塊，使用者必須是列出合作夥伴的 [!DNL Audience Manager] 使用者。建議您選擇此選項作為最佳作法。
1. **[!UICONTROL Scope]** 在區段中，視需要選擇或 **[!UICONTROL Read]** 取消選取與 **[!UICONTROL Write]** 核取方塊。
1. 在 **[!UICONTROL Grant Type]** 區段中，選取想要的授權方式。建議您使用預設設定 [!UICONTROL Password] 和 [!UICONTROL Refresh-token] 選項。

   * **[!UICONTROL Implicit]**：如果您選取此選項，則 [!UICONTROL Redirect URI] 會啓用方塊。使用者在驗證後獲得自動存取Token，並立即傳送至重新導向 [!DNL URI]。
   * **[!UICONTROL Authorization Code]**：如果您選取此選項，則 [!UICONTROL Redirect URI] 會啓用方塊。使用者在進行驗證後會返回用戶端，然後傳送至重新導向 [!DNL URI]。
   * **[!UICONTROL Password]**：使用者會使用使用者輸入的密碼進行驗證，而非透過授權伺服器進行自動驗證嘗試。
   * **[!UICONTROL Refresh_token]**：用來重新整理過期的存取Token長時間。

1. **[!UICONTROL Redirect URI]** 在方塊中指定所需 [!DNL URI]。只有當您選取 **[!UICONTROL Implicit]** 和 **[!UICONTROL Authorization_code]** 授予類型時，才會啓用此選項。**[!UICONTROL Redirect URI]** 此方塊可讓您指定可接受 [!DNL URI] 值的逗號分隔值。這是用戶端 [!DNL URI] 的使用者被重新導向至之後，核准用戶端以 [!DNL API] 進行存取。
1. 指定所要的有效期時間(以秒為單位)，以存取和重新整理Token有效期。

   * **[!UICONTROL Access Token Expiration Time]**：存取Token在發佈後有效的秒數。可以是null，使用平台預設值(12小時)。也可能是-表示存取Token未過期。
   * **[!UICONTROL Refresh Token Expiration Time]**：重新整理Token在發佈後有效的秒數。可以是null，以使用平台預設值(30天)。

1. Click **[!UICONTROL Save]**.

若要刪除 [!UICONTROL OAuth2] 用戶端，請按一下 **[!UICONTROL OAuth2 Clients]**，然後按一 ![](assets/icon_delete.png)**[!UICONTROL Actions]** 下欄中所要的用戶端。

>[!MORE_贊_ this]
>
>* [API需求和建議](../admin-oauth2/aam-admin-api-requirements.md)

