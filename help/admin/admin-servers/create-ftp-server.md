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

使用 [!UICONTROL Servers] Audience Manager管理工具中的頁面來建立新的FTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具有角色 [!UICONTROL DEXADMIN] 才能建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請按一下 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請在列中按一下所需的服 **[!UICONTROL Label]** 務器。
1. 指定此伺服器的所需標籤。
1. 從下拉 **[!UICONTROL Protocol]** 式清單中，選擇所要的通訊協定： **FTP**。

   >[!NOTE]
   >
   >建議您最好將檔案當做 [!DNL Amazon S3] 從合作夥伴取得檔案並傳送給合作夥伴的方法。 [!DNL Amazon S3] 提供簡單的web services介面，可用來隨時隨地儲存和擷取任何數量的資料。 如需詳細資訊，請 [參閱Audience Manager使用指南中的](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)*關於Amazon S3*。

1. 填寫欄位: 

   * **[!UICONTROL Type]:**選擇所需的加密類型：**[!UICONTROL SFTP]**或&#x200B;**[!UICONTROL FTPs/TLS]**者。
   * **[!UICONTROL Domain]:**指定此伺服器所需的網域（主機）。
   * **[!UICONTROL Port]:**為此伺服器指定所需的埠。 每個加密類型都會顯示預設埠。 如有必要，可以更改預設埠。
   * **[!UICONTROL Remote Path]:**為此伺服器指定所需的遠程路徑。 如果您將此欄位留空，Audience Manager會將檔案置於預設目錄中。
   * **[!UICONTROL .tmp File Rename on Completion]:**啟用此選項可在完成時重`.tmp`新命名檔案。
   * **[!UICONTROL Filename Suffix]:**指定要附加來傳輸檔案的文字。
   * **[!UICONTROL Moved to When Finished]:**指定要在完成時移動傳輸檔案的位置的路徑。
   * **[!UICONTROL Authentication]:**指定所需的伺服器驗證方法：**[!UICONTROL Username/Password]**或&#x200B;**[!UICONTROL SSH Key]**者。
   >[!NOTE]
   >
   >請記得將我們的出 [!DNL FTP] 口添加 [!DNL IP] 到允許的IP清單中： **52.44.29.204**。

1. 針對 **[!UICONTROL SSH Key]** 驗證：
   >[!NOTE]
   >
   >配置SSH密鑰驗證時，請務必始終僅以OpenSSH格式生成公共密鑰和私有密鑰。
   1. 從任何或機器產生公用／私 [!DNL Linux] 用金 [!DNL Mac] 鑰對。
   1. 將公 **開金鑰** ，交給用戶端以更新其伺服 [!DNL SFTP] 器。 他們必須在其伺服器上包含公開金鑰的所有文字，包括 `-----BEGIN RSA PRIVATE KEY-----` 和 `-----END RSA PRIVATE KEY-----` 。 作為交換，他們必須提供安裝密鑰時所使用的用戶名。
   1. 使用用戶端提供的使用者名稱欄位更新使用者名稱欄位，使用私密金鑰更新 **金鑰欄位**。
1. 如果 **[!UICONTROL Create]** 要建立新伺服器，請按一下，或者如果 **[!UICONTROL Update]** 要編輯現有伺服器，請按一下。
