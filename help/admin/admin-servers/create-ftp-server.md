---
description: 使用「Audience Manager管理」工具中的「伺服器」頁可建立新的FTP伺服器或編輯現有伺服器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: 建立或編輯 FTP 伺服器
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# 建立或編輯 FTP 伺服器 {#create-or-edit-an-ftp-server}

使用 [!UICONTROL Servers] 頁面，以建立新的FTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須 [!UICONTROL DEXADMIN] 角色以建立新伺服器或編輯現有伺服器。

1. 要建立新伺服器，請按一下 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請按一下 **[!UICONTROL Label]** 的雙曲餘切值。
1. 指定此伺服器所需的標籤。
1. 從 **[!UICONTROL Protocol]** 下拉清單中，選擇所需的協定： **FTP**。

   >[!NOTE]
   >
   >作為最佳實踐，我們建議使用 [!DNL Amazon S3] 作為從合作夥伴獲取檔案並將檔案傳送到合作夥伴的方法。 [!DNL Amazon S3] 提供一個簡單的web服務介面，可用於隨時隨地從web上的任何位置儲存和檢索任意數量的資料。 有關詳細資訊，請參見 [關於AmazonS3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) 的 *Audience Manager使用手冊*。

1. 填寫欄位: 

   * **[!UICONTROL Type]:** 選擇所需的加密類型： **[!UICONTROL SFTP]** 或 **[!UICONTROL FTPs/TLS]**。
   * **[!UICONTROL Domain]:** 為此伺服器指定所需的域（主機）。
   * **[!UICONTROL Port]:** 指定此伺服器所需的埠。 每個加密類型都顯示預設埠。 如有必要，可更改預設埠。
   * **[!UICONTROL Remote Path]:** 指定此伺服器所需的遠程路徑。 如果將此欄位留空，則Audience Manager會將檔案置於預設目錄中。
   * **[!UICONTROL .tmp File Rename on Completion]:** 啟用此選項可更名 `.tmp` 檔案。
   * **[!UICONTROL Filename Suffix]:** 指定要附加以傳輸檔案的文本。
   * **[!UICONTROL Moved to When Finished]:** 指定要在完成時移動傳輸檔案的位置的路徑。
   * **[!UICONTROL Authentication]:** 指定所需的伺服器身份驗證方法： **[!UICONTROL Username/Password]** 或 **[!UICONTROL SSH Key]**。

   >[!NOTE]
   >
   >記住添加出口 [!DNL FTP] [!DNL IP] 列出允許的IP: **52.44.29.204**。

1. 對於 **[!UICONTROL SSH Key]** 驗證：
   >[!NOTE]
   >
   >配置SSH密鑰驗證時，請確保始終只以OpenSSH格式生成公鑰和私鑰。
   1. 從任何 [!DNL Linux] 或 [!DNL Mac] 機器。
   1. 提供 **公鑰** 以更新客戶 [!DNL SFTP] 伺服器。 它們必須包括其伺服器上公鑰中的所有文本，包括 `-----BEGIN RSA PRIVATE KEY-----` 和  `-----END RSA PRIVATE KEY-----` 。 作為交換，它們必須提供安裝密鑰的用戶名。
   1. 使用客戶端提供的用戶名欄位和使用 **私鑰**。
1. 按一下 **[!UICONTROL Create]** 如果要建立新伺服器，或按一下 **[!UICONTROL Update]** 編輯現有伺服器。
