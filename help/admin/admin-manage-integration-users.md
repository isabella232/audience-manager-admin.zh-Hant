---
description: 使用「整合使用者」頁面，在您的Audience Manager組態中檢視使用者清單。您可以編輯或刪除現有使用者，或建立新使用者，前提是您已指派適當的使用者角色。
seo-description: 使用「整合使用者」頁面，在您的Audience Manager組態中檢視使用者清單。您可以編輯或刪除現有使用者，或建立新使用者，前提是您已指派適當的使用者角色。
seo-title: 整合使用者
title: 整合使用者
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 整合使用者 {#integration-users}

使用 [!UICONTROL Integration Users] 頁面來檢視Audience Manager設定中的使用者清單。您可以編輯或刪除現有使用者，或建立新使用者，前提是您已指派適當的使用者角色。

<!-- c_integration_users.xml -->

您可以按一下所要的欄標題，以遞增或遞減順序排序每欄。
使用 [!UICONTROL Search] 方塊底部或清單底部的分頁控制項來尋找所需的使用者。

## 建立或編輯使用者 {#create-edit-user}

使用Audience [!UICONTROL Integration Users] Manager [!UICONTROL Admin] 工具中的頁面建立新使用者或編輯現有使用者的帳戶。

<!-- t_create_user.xml -->

>[!NOTE]
>
>您必須擁有 [!UICONTROL CREATE_USER] 角色才能建立新使用者。您必須擁有 [!UICONTROL EDIT_USER] 該角色才能編輯現有使用者。

1. 若要建立新使用者，請按一下 **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**。若要編輯現有使用者，請按一下 **[!UICONTROL Username]** 欄中所要的使用者。
2. 填寫欄位: 
   * **[!UICONTROL First Name]**：(必要)指定使用者的名字。
   * **[!UICONTROL Last Name]**：(必要)指定使用者的姓氏。
   * **[!UICONTROL Username]**：(必要)指定使用者的使用者名稱。
   * **[!UICONTROL Email Address]**：(必要)指定使用者的電子郵件地址。
   * **[!UICONTROL Phone Number]**：指定使用者的電話號碼。
   * **[!UICONTROL IMS ID]**：指定使用者 [!UICONTROL Internet Messaging Service ID]的身分。
   * **[!UICONTROL User Roles]**：選取所需的使用者角色：
      * **[!UICONTROL DEXADMIN]**：提供管理員存取權，以便在Audience Manager [!UICONTROL Admin] 工具中執行工作。如果您未選取此選項，可以選擇個別角色。這些角色可讓使用者使用 [!DNL API] 呼叫來執行工作，而不是在管理工具中執行工作。
      * **[!UICONTROL CREATE_USERS]**：可讓使用者使用 [!DNL API] 呼叫建立新使用者。
      * **[!UICONTROL DELETE_USERS]**：可讓使用者使用 [!DNL API] 呼叫刪除現有使用者。
      * **[!UICONTROL EDIT_USERS]**：可讓使用者使用 [!DNL API] 呼叫編輯現有使用者。
      * **[!UICONTROL VIEW_USERS]**：讓使用者透過 [!DNL API] 呼叫，在您的Audience Manager設定中檢視其他使用者。
      * **[!UICONTROL CREATE_PARTNERS]**：可讓使用者使用 [!DNL API] 呼叫建立Audience Manager合作夥伴。
      * **[!UICONTROL DELETE_PARTNERS]**：可讓使用者刪除使用 [!DNL API] 呼叫的Audience Manager合作夥伴。
      * **[!UICONTROL EDIT_PARTNERS]**：可讓使用者使用 [!DNL API] 呼叫編輯Audience Manager合作夥伴。
      * **[!UICONTROL VIEW_PARNTERS]**：讓使用者可以使用 [!DNL API] 呼叫來檢視Audience Manager合作夥伴。
   * **狀態：** 選取 **[!UICONTROL Active]** 以讓此使用者已啓動Audience Manager使用者。
3. Click **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

使用Audience [!UICONTROL Integration Users] Manager [!UICONTROL Admin] 工具中的頁面來刪除現有使用者。

<!-- t_delete_user.xml -->

>[!NOTE]
>
>您必須擁有 **[!UICONTROL DELETE_USER]** 角色才能建立新使用者。

1. Click **[!UICONTROL Integration Users]**.
2. 按一下 ![](assets/icon_delete.png) 所需使用者 **[!UICONTROL Actions]** 的欄。
3. Click **[!UICONTROL OK]** to confirm the deletion.