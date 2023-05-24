---
description: 有些客戶可能不想提供其Amazon Simple Storage Service (Amazon S3)存取權或秘密金鑰來Adobe授權將目的地資料上傳至其貯體。
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: 如何授權批次目標的跨帳戶Amazon S3儲存貯體存取
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 如何授權批次目標的跨帳戶Amazon S3儲存貯體存取{#authorize-cross-account-bucket-batch}

有些客戶可能不想提供他們的 [!DNL Amazon S3] Adobe的存取或秘密金鑰，可授權將目的地資料上傳至其貯體。

我們可以提供給客戶的替代方案是 [!UICONTROL Cross-Account Bucket Permissions] 在 [!DNL Amazon S3]. 此程式的說明請參閱 [AWS檔案](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). 若要在Audience Manager中啟用此替代方案，請遵循下列步驟：

1. 前往 **[!UICONTROL Servers]** 並選取 **[!UICONTROL Create Server]**.
1. 選取 **[!UICONTROL S3]** 在 **[!UICONTROL Protocol/Credentials]** 下拉式遮色片。
1. 檢查 **[!UICONTROL Use Internal Adobe Key]** 選項。
1. 在中使用您的客戶帳戶和貯體名稱 [!DNL Amazon S3].
1. 請確定您的客戶白名單中有 [!DNL Amazon S3] 帳戶 `975822914085` 於 [!DNL S3] 貯體。

>[!NOTE]
>
>我們的傳出發佈者會確保許可權層級 `bucket-owner-full-control` 已上傳資料中已設定，因此您的客戶可以擁有該資料。
