---
description: 使用「Audience Manager管理工具」中的「伺服器」頁可建立新的FTP伺服器或編輯現有伺服器。
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

使用「Audience Manager管理工具」中的[!UICONTROL Servers]頁面建立新的FTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具有[!UICONTROL DEXADMIN]角色，才能建立新伺服器或編輯現有伺服器。

1. 要建立新伺服器，請按一下「**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**」。 要編輯現有伺服器，請在&#x200B;**[!UICONTROL Label]**&#x200B;列中按一下所需的伺服器。
1. 為此伺服器指定所需的標籤。
1. 從&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉式清單中，選取所需的通訊協定：**FTP**。

   >[!NOTE]
   >
   >建議您使用[!DNL Amazon S3]作為從合作夥伴取得檔案並將檔案傳送至合作夥伴的方法，這才是最佳作法。 [!DNL Amazon S3] 提供簡單的web服務介面，可用於隨時隨地儲存和檢索任意數量的資料。如需詳細資訊，請參閱&#x200B;*Audience Manager使用手冊*&#x200B;中的[關於Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html)。

1. 填寫欄位: 

   * **[!UICONTROL Type]:** 選取所需的加密類型： **[!UICONTROL SFTP]** 或 **[!UICONTROL FTPs/TLS]**。
   * **[!UICONTROL Domain]:** 指定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]:** 指定此伺服器的所需埠。每種加密類型都會顯示預設埠。 如有必要，您可以變更預設連接埠。
   * **[!UICONTROL Remote Path]:** 指定此伺服器的所需遠端路徑。如果將此欄位留空，Audience Manager會將檔案置於預設目錄中。
   * **[!UICONTROL .tmp File Rename on Completion]:** 啟用此選項可在完成時 `.tmp` 重新命名檔案。
   * **[!UICONTROL Filename Suffix]:** 指定要附加以傳輸檔案的文字。
   * **[!UICONTROL Moved to When Finished]:** 指定要在完成時移動傳輸檔案的位置路徑。
   * **[!UICONTROL Authentication]:** 指定所需的伺服器驗證方法： **[!UICONTROL Username/Password]** 或 **[!UICONTROL SSH Key]**。

   >[!NOTE]
   >
   >請記得將輸出[!DNL FTP] [!DNL IP]新增至允許的IP清單：**52.44.29.204**。

1. 對於&#x200B;**[!UICONTROL SSH Key]**&#x200B;身份驗證：
   >[!NOTE]
   >
   >設定SSH金鑰驗證時，請務必一律僅以OpenSSH格式產生公開金鑰和私密金鑰。
   1. 從任何[!DNL Linux]或[!DNL Mac]電腦生成公用/私鑰對。
   1. 將&#x200B;**公鑰**&#x200B;賦予客戶端以在其[!DNL SFTP]伺服器上更新。 它們必須包含伺服器上公開金鑰的所有文字，包括`-----BEGIN RSA PRIVATE KEY-----`和`-----END RSA PRIVATE KEY-----` 。 在交換中，他們必須提供安裝金鑰時所使用的使用者名稱。
   1. 使用用戶端提供的使用者名稱欄位更新使用者名稱欄位，使用&#x200B;**私密金鑰**&#x200B;更新金鑰欄位。
1. 如果要建立新伺服器，請按一下&#x200B;**[!UICONTROL Create]**；如果要編輯現有伺服器，請按一下&#x200B;**[!UICONTROL Update]**。
