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


# 如何授權批次目標的跨帳戶Amazon S3儲存桶訪問{#authorize-cross-account-bucket-batch}

有些客戶可能不想提供其[!DNL Amazon S3]存取權或機密金鑰給Adobe，以授權將目標資料上傳至其儲存區。

我們可以為客戶提供的替代方案是[!DNL Amazon S3]中的[!UICONTROL Cross-Account Bucket Permissions]。 此過程在[AWS文檔](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)中介紹。 若要在Audience Manager中啟用此替代選項，請遵循下列步驟：

1. 前往&#x200B;**[!UICONTROL Servers]**&#x200B;並選擇&#x200B;**[!UICONTROL Create Server]**。
1. 在&#x200B;**[!UICONTROL Protocol/Credentials]**&#x200B;下拉式遮色片中選取&#x200B;**[!UICONTROL S3]**。
1. 選中&#x200B;**[!UICONTROL Use Internal Adobe Key]**&#x200B;選項。
1. 在[!DNL Amazon S3]中使用客戶的帳戶和貯體名稱。
1. 請確定您的客戶白名單列出[!DNL Amazon S3]帳戶`975822914085`在其[!DNL S3]儲存貯體上。

>[!NOTE]
>
>我們的「對外」發行者會確保已上傳資料上已設定`bucket-owner-full-control`權限層級，讓您的客戶擁有該資料。
