---
description: 有些客戶可能不想提供Amazon Simple Storage Service(Amazon S3)存取權或機密金鑰給Adobe，以授權目標資料上傳至其儲存區。
seo-description: 有些客戶可能不想提供Amazon Simple Storage Service(Amazon S3)存取權或機密金鑰給Adobe，以授權目標資料上傳至其儲存區。
seo-title: 如何授權批次目標的跨帳戶Amazon S3儲存桶訪問
title: 如何授權批次目標的跨帳戶Amazon S3儲存桶訪問
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# How To Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations{#authorize-cross-account-bucket-batch}

有些客戶可能不想提供Adobe的存 [!DNL Amazon S3] 取權或機密金鑰，以授權將目標資料上傳至其儲存區。

我們提供給客戶的另一種選擇 [!UICONTROL Cross-Account Bucket Permissions] 是 [!DNL Amazon S3]。 此過程在 [AWS文檔中描述](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)。 若要在Audience Manager中啟用此替代選項，請遵循下列步驟：

1. 前往並 **[!UICONTROL Servers]** 選取 **[!UICONTROL Create Server]**。
1. 在下 **[!UICONTROL S3]** 拉式遮 **[!UICONTROL Protocol/Credentials]** 色片中選取。
1. 勾選 **[!UICONTROL Use Internal Adobe Key]** 選項。
1. 在中使用客戶的帳戶和時段名稱 [!DNL Amazon S3]。
1. 請確定您的客戶白名單列在 [!DNL Amazon S3] 客戶 `975822914085` 的儲存 [!DNL S3] 桶上。

>[!NOTE]
>
>我們的「對外」發行者會確保已上 `bucket-owner-full-control` 傳資料已設定權限層級，讓您的客戶擁有該資料。
