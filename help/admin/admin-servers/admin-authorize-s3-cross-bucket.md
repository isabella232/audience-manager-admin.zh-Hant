---
description: 有些客戶可能不想提供Amazon Simple Storage Service(Amazon S3)存取或秘密金鑰給Adobe授權將目的地資料上傳至其桶。
seo-description: 有些客戶可能不想提供Amazon Simple Storage Service(Amazon S3)存取或秘密金鑰給Adobe授權將目的地資料上傳至其桶。
seo-title: 如何授權跨帳戶目標的跨帳戶Amazon S儲存貯體存取權
title: 如何授權跨帳戶目標的跨帳戶Amazon S儲存貯體存取權
uuid: da2bcda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 如何授權跨帳戶目標的跨帳戶Amazon S儲存貯體存取權{#authorize-cross-account-bucket-batch}

有些客戶可能不想向Adobe提供 [!DNL Amazon S3] 存取或秘密金鑰，以授權上傳目的地資料至其桶。

我們可以提供客戶的替代 [!UICONTROL Cross-Account Bucket Permissions][!DNL Amazon S3]方案。[AWS文件](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)說明此程序。若要在Audience Manager中啓用此替代項目，請遵循下列步驟：

1. 前往 **[!UICONTROL Servers]** 並選擇 **[!UICONTROL Create Server]**。
1. 在 **[!UICONTROL S3]****[!UICONTROL Protocol/Credentials]** 下拉式遮色片中選取。
1. 請查看 **[!UICONTROL Use Internal Adobe Key]** 選項。
1. 請使用客戶的帳戶和貯體名稱 [!DNL Amazon S3]。
1. 請確定您的客戶白名單會在其儲存貯體中列出 [!DNL Amazon S3] 帳戶 `975822914085`[!DNL S3] 。

>[!NOTE]
>
>我們的對外出版sher可確保在上傳的資料上設定權限等級 `bucket-owner-full-control` ，讓客戶擁有該資料。
