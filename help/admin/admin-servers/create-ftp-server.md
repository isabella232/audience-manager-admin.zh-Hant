---
description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的FTP伺服器或編輯現有伺服器。
seo-description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的FTP伺服器或編輯現有伺服器。
seo-title: 建立或編輯FTP伺服器
title: 建立或編輯FTP伺服器
uuid: 9273abb2-963d-4d83-bb5 a-b3817 f0 b90 e6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 建立或編輯FTP伺服器 {#create-or-edit-an-ftp-server}

使用Audience Manager管理工具中的 [!UICONTROL Servers] 頁面建立新的FTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具備此 [!UICONTROL DEXADMIN] 角色才能建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請按一下 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**。若要編輯現有的伺服器，請按一下 **[!UICONTROL Label]** 欄中所要的伺服器。
1. 指定此伺服器所要的標籤。
1. 從 **[!UICONTROL Protocol]** 下拉式清單中，選取所需的通訊協定： **FTP**。

   >[!NOTE]
   >
   >作為最佳實務，我們建議您使用一 [!DNL Amazon S3] 種方法，將檔案從檔案傳送給合作夥伴。[!DNL Amazon S3] 提供簡單的web services介面，可用來隨時隨地儲存和擷取任何數量的資料。如需詳細資訊，請參閱 [Audience](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) *Manager使用指南中的關於Amazon S3*。

1. 填寫欄位: 

   * **[!UICONTROL Type]：** 選取所需的加密類型： **[!UICONTROL SFTP]****[!UICONTROL FTPs/TLS]**&#x200B;或
   * **[!UICONTROL Domain]：** 指定此伺服器的所需網域(主機)。
   * **[!UICONTROL Port]：** 指定此伺服器所要的連接埠。會針對每個加密類型顯示預設連接埠。您可視需要變更預設連接埠。
   * **[!UICONTROL Remote Path]：** 指定此伺服器所需的遠端路徑。如果您將此欄位保留空白，Audience Manager會將檔案置於預設目錄中。
   * **[!UICONTROL .tmp File Rename on Completion]：** 啓用此選項可在完成時重新命名 `.tmp` 檔案。
   * **[!UICONTROL Filename Suffix]：** 指定您要附加的文字以傳輸檔案。
   * **[!UICONTROL Moved to When Finished]：** 指定傳送檔案在完成時移動的位置路徑。
   * **[!UICONTROL Authentication]：** 指定所需的伺服器驗證方法： **[!UICONTROL Username/Password]****[!UICONTROL SSH Key]**&#x200B;或
   >[!NOTE]
   >
   >記得將我們的地理位置列入白名單 [!DNL FTP][!DNL IP]： **52.44.29.204**.

1. 用於 **[!UICONTROL SSH Key]** 驗證：
   1. 從任何 [!DNL Linux] 或 [!DNL Mac] 機器產生公開/私密金鑰配對。
   1. 將 **公開金鑰** 提供給用戶端，以便在 [!DNL SFTP] 其伺服器上更新。他們必須包含伺服器上公開金鑰中的所有文字，包括 `-----BEGIN RSA PRIVATE KEY-----` 和 `-----END RSA PRIVATE KEY-----` 。交換時，他們必須提供安裝金鑰的使用者名稱。
   1. 以用戶端提供的使用者名稱欄位和 **私密金鑰的索引鍵欄位來更新使用者名稱欄位**。
1. 如果 **[!UICONTROL Create]** 您要建立新伺服器，請按一下， **[!UICONTROL Update]** 如果您正在編輯現有伺服器。
