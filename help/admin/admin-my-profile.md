---
description: 編輯Audience Manager管理工具設定檔的詳細資訊或變更密碼。
seo-description: Edit the details of your Audience Manager Admin tool profile or change your password.
seo-title: My Profile
title: 我的設定檔
uuid: ccaa611d-c855-484e-9696-081d9b4e0935
exl-id: d213f734-af52-4f43-8733-af67ce6f4e98
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 3%

---

# 我的設定檔 {#my-profile}

編輯Audience Manager管理工具設定檔的詳細資訊或變更密碼。

<!-- c_my_profile.xml -->

## 編輯設定檔 {#edit-profile}

檢視及編輯您的Audience Manager管理工具設定檔，包括名字和姓氏、使用者名稱、電子郵件地址、電話號碼、 [!UICONTROL IMS ID]、使用者角色和狀態。

<!-- t_edit_profile.xml -->

1. 按一下 **[!UICONTROL My Profile]**.

   ![步驟結果](assets/profile.png)

2. 填寫欄位: 
   * **[!UICONTROL First Name]：** （必要）指定您的名字。
   * **[!UICONTROL Last Name]：** （必要）指定您的姓氏。
   * **[!UICONTROL Username]：** （必要）指定您的第一個使用者名稱。
   * **[!UICONTROL Email Address]：** （必要）指定您的電子郵件地址。
   * **[!UICONTROL Phone Number]：** 指定您的電話號碼。
   * **[!UICONTROL IMS ID]：** 指定您的網際網路傳訊服務ID。
   * **[!UICONTROL User Roles]：** 選取所需的使用者角色：
      * **[!UICONTROL DEXADMIN]：** 提供管理員存取權，以便在Audience Manager管理工具中執行工作。 如果您未選取此選項，則可以選擇個別角色。 這些角色可讓使用者透過以下方式執行任務： [!DNL API] 呼叫，但不在管理工具中。
      * **[!UICONTROL CREATE_USERS]：** 可讓使用者使用 [!DNL API] 呼叫。
      * **[!UICONTROL DELETE_USERS]：** 可讓使用者使用刪除現有使用者 [!DNL API] 呼叫。
      * **[!UICONTROL EDIT_USERS]：** 可讓使用者使用編輯現有使用者 [!DNL API] 呼叫。
      * **[!UICONTROL VIEW_USERS]：** 可讓使用者在您的Audience Manager設定中使用 [!DNL API] 呼叫。
      * **[!UICONTROL CREATE_PARTNERS]：** 可讓使用者使用建立Audience Manager合作夥伴 [!DNL API] 呼叫。
      * **[!UICONTROL DELETE_PARTNERS]：** Audience Manager可讓使用者使用 [!DNL API] 呼叫。
      * **[!UICONTROL EDIT_PARTNERS]：** 可讓使用者使用編輯Audience Manager合作夥伴 [!DNL API] 呼叫。
      * **[!UICONTROL VIEW_PARNTERS]：** 可讓使用者使用檢視Audience Manager合作夥伴 [!DNL API] 呼叫。
   * **[!UICONTROL Status]：** 選取所需的狀態：
      * **[!UICONTROL Active]：** 指定此使用者在作用中Audience Manager使用者。
      * **[!UICONTROL Deactivated]：** 指定此使用者為Audience Management中的已停用使用者。
      * **[!UICONTROL Expired]：** 指定此使用者的Audience Manager帳戶已過期。
      * **[!UICONTROL Locked Out]：** 指定鎖定此使用者的Audience Manager帳戶。
3. 按一下 **[!UICONTROL Submit]**.

## 變更密碼 {#change-password}

變更您的Audience Manager管理工具密碼。

<!-- t_change_password.xml -->

1. 按一下 **[!UICONTROL My Profile]**.
1. 按一下 **[!UICONTROL Change Password]**.

   ![](assets/change_password.png)

   您的Audience Manager密碼必須是：

   * 長度至少為8個字元；
   * 至少包含一個大寫字元；
   * 至少包含一個小寫字元；
   * 至少包含一個數字；
   * 至少包含一個特殊字元；
   * 以英數字元開始和結束；
   * 以英數字元開始和結束。

1. 指定您的舊密碼。
1. 指定您的新密碼，然後確認新密碼。
1. 按一下 **[!UICONTROL OK]**.
