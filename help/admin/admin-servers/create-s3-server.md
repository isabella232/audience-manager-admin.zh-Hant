---
description: 使用「Audience Manager管理」工具中的「伺服器」頁可以建立新的S3伺服器或編輯現有伺服器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new S3 server or to edit an existing server.
seo-title: Create or Edit an S3 Server
title: 建立或編輯 S3 伺服器
uuid: 94fee787-eb26-45aa-b602-d61ab12969ea
exl-id: 89310de0-e24e-4d4b-8171-56faf0b441f6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 7%

---

# 建立或編輯 S3 伺服器 {#create-or-edit-an-s-server}

使用 [!UICONTROL Servers] Audience Manager管理工具中的頁面以建立新 [!DNL S3] 或編輯現有伺服器。

>[!NOTE]
>
>您必須 [!UICONTROL DEXADMIN] 角色以建立新伺服器或編輯現有伺服器。

1. 要建立新伺服器，請按一下 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請按一下 **[!UICONTROL Label]** 的雙曲餘切值。
1. 指定此伺服器所需的標籤。
1. 從 **[!UICONTROL Protocol]** 下拉清單中，選擇所需的協定： **[!UICONTROL S3]**。

   >[!NOTE]
   >
   >我們建議使用 [!DNL Amazon S3] 作為從合作夥伴獲取檔案並將檔案傳送到合作夥伴的方法。 [!DNL Amazon S3] 提供一個簡單的web服務介面，可用於隨時隨地從web上的任何位置儲存和檢索任意數量的資料。 有關詳細資訊，請參見 [關於AmazonS3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) 的 *Audience Manager使用手冊*。

1. 填寫欄位: 

   * **[!UICONTROL Account]:** 指定所需 [!DNL S3] 帳戶。
   * **[!UICONTROL Bucket]:** 指定所需 [!DNL S3] 桶。
   * **[!UICONTROL Directory]:** 指定所需 [!DNL S3] 的子菜單。
   * **[!UICONTROL Access Key]:** 指定所需 [!DNL S3] 訪問密鑰。
   * **[!UICONTROL Secret Key]:** 指定所需 [!DNL S3] 密鑰。

1. 按一下 **[!UICONTROL Create]** 如果要建立新伺服器，或按一下 **[!UICONTROL Update]** 編輯現有伺服器。
