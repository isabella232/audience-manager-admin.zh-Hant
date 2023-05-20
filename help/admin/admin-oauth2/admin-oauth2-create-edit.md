---
description: 使用「OAuth2客戶端」頁可以查看Audience Manager配置中的OAuth2客戶端清單。 您可以編輯或刪除現有客戶端或建立新客戶端，前提是您已分配了相應的用戶角色。
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

使用 [!UICONTROL OAuth2 Clients] 頁面以查看 [!UICONTROL OAuth2] 客戶 [!DNL Audience Manager] 配置。 您可以編輯或刪除現有客戶端或建立新客戶端，前提是您已分配了相應的用戶角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>確保您的客戶閱讀 [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) Audience Manager使用手冊中的文檔。

[!DNL OAuth2] 是一個開放的授權標準，可提供安全的委託訪問 [!DNL Audience Manager] 資源。

![](assets/oauth.png)

通過按一下所需列的標題，可以按升序或降序對每列進行排序。

使用 [!UICONTROL Search] 對話框或清單底部的分頁控制項以查找所需的客戶端。

## 建立或編輯OAuth2客戶端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用 [!UICONTROL OAuth2 Clients] 頁面的Audience Manager [!UICONTROL Admin] 建立新工具 [!UICONTROL Oauth2] 或編輯現有客戶端。

1. 建立新 [!UICONTROL OAuth2] 客戶端，按一下 **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**。 編輯現有 [!UICONTROL OAuth2] 客戶端，按一下 **[!UICONTROL Client ID]** 的雙曲餘切值。
1. 為此指定所需名稱 [!UICONTROL OAuth2] 客戶端。 請注意，這只是記錄的名稱。
1. 指定 [!UICONTROL OAuth2] 客戶端的電子郵件地址。 電子郵件地址有限。
1. 從 **[!UICONTROL Partner]** 下拉清單，選擇所需的合作夥伴。
1. 在 **[!UICONTROL Client ID]** 框中，指定所需的ID。 這是提交時使用的值 [!DNL API] 請求。 在選擇了 [!UICONTROL Partner] 的子菜單。 正確格式為&lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>。
1. 選擇或取消選擇 **[!UICONTROL Restrict to Partner Users]** 按鈕。 如果選中此複選框，則用戶必須是 [!DNL Audience Manager] 為所選夥伴列出的用戶。 作為最佳做法，我們建議您選擇此選項。
1. 在 **[!UICONTROL Scope]** ，選擇或取消選擇 **[!UICONTROL Read]** 和 **[!UICONTROL Write]** 按鈕。
1. 在 **[!UICONTROL Grant Type]** 的子菜單。 建議您使用 [!UICONTROL Password] 和 [!UICONTROL Refresh-token] 頁籤

   * **[!UICONTROL Implicit]**:如果選擇此選項， [!UICONTROL Redirect URI] 的子菜單。 用戶在經過認證後被賦予一個自動訪問令牌並被立即發送到重定向 [!DNL URI]。
   * **[!UICONTROL Authorization Code]**:如果選擇此選項， [!UICONTROL Redirect URI] 的子菜單。 用戶在經過身份驗證後返回給客戶機，然後被發送到重定向 [!DNL URI]。
   * **[!UICONTROL Password]**:使用用戶輸入的密碼而不是通過授權伺服器自動驗證嘗試來驗證用戶。
   * **[!UICONTROL Refresh_token]**:用於在較長的時間段內刷新過期的訪問令牌。

1. 在 **[!UICONTROL Redirect URI]** 框中，指定所需 [!DNL URI]。 僅當選擇 **[!UICONTROL Implicit]** 和 **[!UICONTROL Authorization_code]** 授予類型。 的 **[!UICONTROL Redirect URI]** 框，用於指定可接受的逗號分隔值 [!DNL URI] 值。 這是 [!DNL URI] 在為客戶機批准之後，將客戶機的用戶重定向到 [!DNL API] 訪問。
1. 指定訪問和刷新令牌過期所需的過期時間（以秒為單位）。

   * **[!UICONTROL Access Token Expiration Time]**:發出訪問令牌後有效的秒數。 如果使用平台預設值（12小時），則可能為空。 也可以是–1，以指示訪問令牌未過期。
   * **[!UICONTROL Refresh Token Expiration Time]**:發出刷新令牌後有效的秒數。 如果使用平台預設值（30天），則可能為空。

1. 按一下 **[!UICONTROL Save]**.

刪除 [!UICONTROL OAuth2] 客戶端，按一下 **[!UICONTROL OAuth2 Clients]**，然後按一下  ![](assets/icon_delete.png) 的 **[!UICONTROL Actions]** 列。

>[!MORELIKETHIS]
>
>* [API 需求與建議](../admin-oauth2/aam-admin-api-requirements.md)

