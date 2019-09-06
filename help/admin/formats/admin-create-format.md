---
description: 使用Audience Manager管理工具中的「格式」頁面，建立新格式或編輯現有格式。
seo-description: 使用Audience Manager管理工具中的「格式」頁面，建立新格式或編輯現有格式。
seo-title: 建立或編輯格式
title: 建立或編輯格式
uuid: ca1b1feb-bcd3-4a41-b1 e8-80565f6 c23 ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# 建立或編輯格式 {#create-or-edit-a-format}

使用Audience Manager管理工具中的 [!UICONTROL Formats] 頁面建立新格式或編輯現有格式。

<!-- t_create_format.xml -->

>[!TIP]
>
>為您的對外資料選擇格式時，可以盡可能地重復使用現有格式。使用已經證實可行的格式，可確保您的對外資料產生成功。若要確切檢視現有格式的格式，請按一下選單列 [!UICONTROL Formats] 中的選項，然後依名稱或ID編號搜尋格式。格式格式格式不正確或巨集會提供格式錯誤的輸出，或防止資訊完全輸出。

1. 若要建立新格式，請按一下 **[!UICONTROL Formats]** &gt; **[!UICONTROL Add Format]**。若要編輯現有格式，請按一下 **[!UICONTROL Name]** 欄中所要的格式。

   ![](assets/create_format.png)

1. 填寫欄位: 
   * **名稱：** (必要)為格式提供描述性名稱。
   * **類型：** (必要)選擇所要的格式：
      * **[!UICONTROL File]**：透過 [!DNL FTP] 檔案傳送資料。
      * **[!UICONTROL HTTP]**：在 [!DNL JSON] 包裝函式中內嵌資料。

1. (條件性)如果您選擇 **[!UICONTROL File]**，請填寫欄位：

   >[!NOTE]
   >
   >如需可用巨集的清單，請參閱 [「檔案格式Macros](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) 」和 [「HTTP格式巨集](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE)」。

   * **[!UICONTROL File Name]：** 指定資料傳輸檔案的檔案名稱。
   * **標題：** 指定出現在資料傳輸檔案第一列的文字。
   * **[!UICONTROL Data Row]：** 指定出現在檔案每個對外列中的文字。
   * **[!UICONTROL Maximum File Size (In MB)]：** 指定資料傳輸檔案的最大檔案大小。壓縮的檔案必須小於100MB。未壓縮檔案大小沒有限制。
   * **[!UICONTROL Compression]：** 選擇所要的壓縮類型：gz或zip檔。若要傳送至 [!UICONTROL AWS S3]，您必須使用.gz或解壓縮檔案。
   * **[!UICONTROL .info Receipt]：** 指定產生transfer-control([!DNL .info])檔案。[!DNL .info] 檔案提供檔案傳輸的中繼資料資訊，讓合作夥伴可以驗證Audience Manager是否正確地處理檔案傳輸。如需詳細資訊，請參閱 [「傳輸控制檔案傳輸記錄檔傳輸」](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html)。
   * **[!UICONTROL MD5 Checksum Receipt]：** 指定產生 [!DNL MD5] checksum收據。[!DNL MD5] 核取總和收據，讓合作夥伴可驗證Audience Manager是否正確地處理完整傳輸。

1. (條件性)如果您選擇 **[!UICONTROL HTTP]**，請填寫欄位：

   * **[!UICONTROL Method]：** 選擇要用於傳輸程序的 [!DNL API] 方法：
      * **[!UICONTROL POST]：** 如果選取 [!DNL POST]，選取內容類型([!DNL XML] 或 [!DNL JSON])，然後指定請求主體。
      * **[!UICONTROL GET]：** 如果您選取 [!DNL GET]，請指定查詢參數。

1. 如果 **[!UICONTROL Create]** 您要建立新格式，請按一下， **[!UICONTROL Save Updates]** 如果您正在編輯現有格式。

## 刪除格式 {#delete-format}

1. Click **[!UICONTROL Formats]**.
2. 按一 ![](assets/icon_delete.png)**[!UICONTROL Actions]** 下所要格式的欄。
3. Click **[!UICONTROL OK]** to confirm the deletion.
