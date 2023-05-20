---
description: 某些客戶可能不想提供其Amazon簡單儲存服務(AmazonS3)訪問或密鑰以Adobe授權目標資料上載到其儲存桶。
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: 如何授權批目標的跨帳戶AmazonS3時段訪問
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 如何授權批目標的跨帳戶AmazonS3時段訪問{#authorize-cross-account-bucket-batch}

有些客戶可能不想提供 [!DNL Amazon S3] 訪問或密鑰以Adobe授權將目標資料上載到其儲存桶。

我們可以為客戶提供的替代方案是 [!UICONTROL Cross-Account Bucket Permissions] 在 [!DNL Amazon S3]。 此過程在 [AWS文檔](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)。 要在Audience Manager中啟用此備選項，請執行以下步驟：

1. 轉到 **[!UICONTROL Servers]** 選擇 **[!UICONTROL Create Server]**。
1. 選擇 **[!UICONTROL S3]** 的 **[!UICONTROL Protocol/Credentials]** 下拉口罩。
1. 檢查 **[!UICONTROL Use Internal Adobe Key]** 的雙曲餘切值。
1. 在中使用客戶的帳戶和時段名稱 [!DNL Amazon S3]。
1. 確保客戶白名單 [!DNL Amazon S3] 帳戶 `975822914085` 在 [!DNL S3] 桶。

>[!NOTE]
>
>我們的出站發佈者確保權限級別 `bucket-owner-full-control` 設定在上載的資料上，以便您的客戶可以擁有該資料。
