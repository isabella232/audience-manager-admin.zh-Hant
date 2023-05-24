---
description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的FTP伺服器或編輯現有的伺服器。
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

使用 [!UICONTROL Servers] 頁面，以建立新的FTP伺服器或編輯現有的伺服器。Audience Manager管理工具。

>[!NOTE]
>
>您必須擁有 [!UICONTROL DEXADMIN] 角色，以建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請按一下 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 若要編輯現有伺服器，請在 **[!UICONTROL Label]** 欄。
1. 指定此伺服器的所需標籤。
1. 從 **[!UICONTROL Protocol]** 下拉式清單，選取所需的通訊協定： **FTP**.

   >[!NOTE]
   >
   >作為最佳實務，我們建議使用 [!DNL Amazon S3] 作為從合作夥伴取得檔案並將檔案傳送給合作夥伴的方法。 [!DNL Amazon S3] 提供簡單的Web服務介面，可用於隨時隨地從網路上的任何位置儲存及擷取任何數量的資料。 如需詳細資訊，請參閱 [關於Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) 在 *Audience Manager使用手冊*.

1. 填寫欄位: 

   * **[!UICONTROL Type]：** 選取所需的加密型別： **[!UICONTROL SFTP]** 或 **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]：** 指定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]：** 指定此伺服器的所需連線埠。 每個加密型別都會顯示預設連線埠。 您可以視需要變更預設連線埠。
   * **[!UICONTROL Remote Path]：** 指定此伺服器的所需遠端路徑。 如果您將此欄位留空，Audience Manager會將檔案置於預設目錄中。
   * **[!UICONTROL .tmp File Rename on Completion]：** 啟用此選項以重新命名 `.tmp` 檔案完成時。
   * **[!UICONTROL Filename Suffix]：** 指定要附加以傳輸檔案的文字。
   * **[!UICONTROL Moved to When Finished]：** 指定要在完成時移動傳輸檔案的位置的路徑。
   * **[!UICONTROL Authentication]：** 指定所需的伺服器驗證方法： **[!UICONTROL Username/Password]** 或 **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >記得新增出口 [!DNL FTP] [!DNL IP] 至您的允許IP清單： **52.44.29.204**.

1. 對象 **[!UICONTROL SSH Key]** 驗證：
   >[!NOTE]
   >
   >設定SSH金鑰驗證時，請務必只以OpenSSH格式產生公開和私密金鑰。
   1. 從任何產生公開/私密金鑰組 [!DNL Linux] 或 [!DNL Mac] 電腦。
   1. 提供 **公開金鑰** 至使用者端以更新其 [!DNL SFTP] 伺服器。 它們必須包含其伺服器上公開金鑰的所有文字，包括 `-----BEGIN RSA PRIVATE KEY-----` 和  `-----END RSA PRIVATE KEY-----` . 作為交換，他們必須提供安裝金鑰所用的使用者名稱。
   1. 將使用者名稱欄位更新為使用者端提供的欄位，並將金鑰欄位更新為 **私密金鑰**.
1. 按一下 **[!UICONTROL Create]** 如果您要建立新伺服器，或按一下 **[!UICONTROL Update]** 如果您正在編輯現有伺服器。
