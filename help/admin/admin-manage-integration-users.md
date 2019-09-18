---
description: 使用「整合使用者」頁面，可檢視Audience manager設定中的使用者清單。 您可以編輯或刪除現有用戶或建立新用戶，前提是您已分配了適當的用戶角色。
seo-description: 使用「整合使用者」頁面，可檢視Audience manager設定中的使用者清單。 您可以編輯或刪除現有用戶或建立新用戶，前提是您已分配了適當的用戶角色。
seo-title: 整合使用者
title: 整合使用者
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 整合使用者 {#integration-users}

使用頁 [!UICONTROL Integration Users] 面可檢視Audience manager設定中的使用者清單。 您可以編輯或刪除現有用戶或建立新用戶，前提是您已分配了適當的用戶角色。

<!-- c_integration_users.xml -->

您可以按一下所需欄的標題，以遞增或遞減順序來排序每個欄。
使用 [!UICONTROL Search] 清單底部的方塊或分頁控制項，以尋找所需的使用者。

## 建立或編輯使用者 {#create-edit-user}

使用 [!UICONTROL Integration Users] Audience manager工具中的頁 [!UICONTROL Admin] 面來建立新使用者或編輯現有使用者帳戶。

<!-- t_create_user.xml -->

>[!NOTE]
>
>您必須擁有角 [!UICONTROL CREATE_USER] 色才能建立新使用者。 您必須擁有角 [!UICONTROL EDIT_USER] 色才能編輯現有使用者。

1. 若要建立新使用者，請按一下 **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**。 若要編輯現有使用者，請按一下欄中所要的 **[!UICONTROL Username]** 使用者。
2. 填寫欄位: 
   * **[!UICONTROL First Name]**:（必要）指定使用者的名字。
   * **[!UICONTROL Last Name]**:（必要）指定使用者的姓氏。
   * **[!UICONTROL Username]**:（必要）指定使用者的使用者名稱。
   * **[!UICONTROL Email Address]**:（必要）指定使用者的電子郵件地址。
   * **[!UICONTROL Phone Number]**:指定使用者的電話號碼。
   * **[!UICONTROL IMS ID]**:指定使用者的 [!UICONTROL Internet Messaging Service ID]。
   * **[!UICONTROL User Roles]**:選擇所需的用戶角色：
      * **[!UICONTROL DEXADMIN]**:提供管理員存取權，可在Audience Manager工具中執行 [!UICONTROL Admin] 工作。 如果未選擇此選項，則可以選擇單個角色。 這些角色可讓使用者使用呼叫來執 [!DNL API] 行工作，但不會在「管理」工具中執行。
      * **[!UICONTROL CREATE_USERS]**:可讓使用者使用呼叫建立新 [!DNL API] 使用者。
      * **[!UICONTROL DELETE_USERS]**:可讓使用者使用呼叫刪除現有 [!DNL API] 使用者。
      * **[!UICONTROL EDIT_USERS]**:可讓使用者使用呼叫來編輯現有 [!DNL API] 使用者。
      * **[!UICONTROL VIEW_USERS]**:可讓使用者使用呼叫，在您的Audience manager設定中檢視其他使 [!DNL API] 用者。
      * **[!UICONTROL CREATE_PARTNERS]**:可讓使用者使用呼叫建立Audience Manager [!DNL API] 合作夥伴。
      * **[!UICONTROL DELETE_PARTNERS]**:可讓使用者使用呼叫刪除Audience manager合 [!DNL API] 作夥伴。
      * **[!UICONTROL EDIT_PARTNERS]**:可讓使用者使用呼叫來編輯Audience manager合 [!DNL API] 作夥伴。
      * **[!UICONTROL VIEW_PARNTERS]**:可讓使用者使用呼叫來檢視Audience manager合作 [!DNL API] 夥伴。
   * **** 狀態：選取 **[!UICONTROL Active]** 可讓此使用者成為已啟動的Audience manager使用者。
3. Click **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

使用Audience [!UICONTROL Integration Users] Manager工具中的頁 [!UICONTROL Admin] 面來刪除現有使用者。

<!-- t_delete_user.xml -->

>[!NOTE]
>
>您必須擁有角 **[!UICONTROL DELETE_USER]** 色才能建立新使用者。

1. Click **[!UICONTROL Integration Users]**.
2. 按一 ![](assets/icon_delete.png) 下所 **[!UICONTROL Actions]** 要使用者的欄。
3. Click **[!UICONTROL OK]** to confirm the deletion.