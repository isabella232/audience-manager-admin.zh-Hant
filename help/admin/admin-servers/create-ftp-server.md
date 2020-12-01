---
description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的FTP伺服器或編輯現有伺服器。
seo-description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的FTP伺服器或編輯現有伺服器。
seo-title: 建立或編輯 FTP 伺服器
title: 建立或編輯 FTP 伺服器
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: 78d694670e7abdc18938c5be729ad499e2647825
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 5%

---


# 建立或編輯 FTP 伺服器{#create-or-edit-an-ftp-server}

使用Audience Manager管理工具中的[!UICONTROL Servers]頁面建立新的FTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具有[!UICONTROL DEXADMIN]角色，才能建立新伺服器或編輯現有伺服器。

1. 要建立新伺服器，請按一下&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請在&#x200B;**[!UICONTROL Label]**&#x200B;列中按一下所需的伺服器。
1. 指定此伺服器的所需標籤。
1. 從&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉式清單中，選取所需的通訊協定：**FTP**。

   >[!NOTE]
   >
   >建議您使用[!DNL Amazon S3]作為從合作夥伴取得檔案並傳送檔案的方法，這是最佳實務。 [!DNL Amazon S3] 提供簡單的web services介面，可用來隨時隨地儲存和擷取任何數量的資料。如需詳細資訊，請參閱&#x200B;*Audience Manager使用指南*&#x200B;中的[關於Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)。

1. 填寫欄位: 

   * **[!UICONTROL Type]：選** 擇所需的加密類型： **[!UICONTROL SFTP]** 或 **[!UICONTROL FTPs/TLS]**&#x200B;者。
   * **[!UICONTROL Domain]：指** 定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]：指** 定此伺服器的所需埠。每個加密類型都會顯示預設埠。 如有必要，可以更改預設埠。
   * **[!UICONTROL Remote Path]：指** 定此伺服器的所需遠程路徑。如果您將此欄位留空，Audience Manager會將檔案置於預設目錄中。
   * **[!UICONTROL .tmp File Rename on Completion]：啟** 用此選項可在完成時重 `.tmp` 新命名檔案。
   * **[!UICONTROL Filename Suffix]：指** 定要附加來傳輸檔案的文字。
   * **[!UICONTROL Moved to When Finished]：指** 定要在完成時移動傳輸檔案的路徑。
   * **[!UICONTROL Authentication]：指** 定所需的伺服器驗證方法： **[!UICONTROL Username/Password]** 或 **[!UICONTROL SSH Key]**&#x200B;者。

   >[!NOTE]
   >
   >請記得將我們的出口[!DNL FTP] [!DNL IP]添加到允許的IP清單中：**52.44.29.204**。

1. 對於&#x200B;**[!UICONTROL SSH Key]**&#x200B;驗證：
   >[!NOTE]
   >
   >配置SSH密鑰驗證時，請務必始終僅以OpenSSH格式生成公共密鑰和私有密鑰。
   1. 從任何[!DNL Linux]或[!DNL Mac]機器產生公用／私用金鑰對。
   1. 將&#x200B;**公共密鑰**&#x200B;提供給客戶機以在其[!DNL SFTP]伺服器上進行更新。 它們必須在其伺服器上包含來自公鑰的所有文本，包括`-----BEGIN RSA PRIVATE KEY-----`和`-----END RSA PRIVATE KEY-----`。 作為交換，他們必須提供安裝密鑰時所使用的用戶名。
   1. 使用客戶端提供的用戶名欄位更新用戶名欄位，使用&#x200B;**私鑰**&#x200B;更新密鑰欄位。
1. 如果要建立新伺服器，請按一下&#x200B;**[!UICONTROL Create]** ，如果要編輯現有伺服器，請按一下&#x200B;**[!UICONTROL Update]**。
