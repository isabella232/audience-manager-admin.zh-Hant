---
description: 使用「Audience Manager管理工具」中的「伺服器」頁面，建立新的S3伺服器或編輯現有的伺服器。
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

使用 [!UICONTROL Servers] 頁面以建立新的Audience Manager管理工具 [!DNL S3] ，或是編輯現有的伺服器。

>[!NOTE]
>
>您必須擁有 [!UICONTROL DEXADMIN] 角色，以建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請按一下 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 若要編輯現有伺服器，請在 **[!UICONTROL Label]** 欄。
1. 指定此伺服器的所需標籤。
1. 從 **[!UICONTROL Protocol]** 下拉式清單，選取所需的通訊協定： **[!UICONTROL S3]**.

   >[!NOTE]
   >
   >我們建議使用 [!DNL Amazon S3] 作為從合作夥伴取得檔案並將檔案傳送給合作夥伴的方法。 [!DNL Amazon S3] 提供簡單的Web服務介面，可用於隨時隨地從網路上的任何位置儲存及擷取任何數量的資料。 如需詳細資訊，請參閱 [關於Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) 在 *Audience Manager使用手冊*.

1. 填寫欄位: 

   * **[!UICONTROL Account]：** 指定所需的 [!DNL S3] 帳戶。
   * **[!UICONTROL Bucket]：** 指定所需的 [!DNL S3] 貯體。
   * **[!UICONTROL Directory]：** 指定所需的 [!DNL S3] 目錄。
   * **[!UICONTROL Access Key]：** 指定所需的 [!DNL S3] 存取金鑰。
   * **[!UICONTROL Secret Key]：** 指定所需的 [!DNL S3] 秘密金鑰。

1. 按一下 **[!UICONTROL Create]** 如果您要建立新伺服器，或按一下 **[!UICONTROL Update]** 如果您正在編輯現有伺服器。
