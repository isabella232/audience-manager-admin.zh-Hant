---
description: 使用Audience Manager管理工具中的「格式」頁面來建立新格式或編輯現有格式。
seo-description: 使用Audience Manager管理工具中的「格式」頁面來建立新格式或編輯現有格式。
seo-title: 建立或編輯格式
title: 建立或編輯格式
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# 建立或編輯格式 {#create-or-edit-a-format}

使用 [!UICONTROL Formats] Audience Manager管理工具中的頁面來建立新格式或編輯現有格式。

<!-- t_create_format.xml -->

>[!TIP]
>
>為外界資料選擇格式時，最好盡可能重新使用現有格式。 使用已證實可行的格式，可確保您的傳出資料能成功產生。 若要確切瞭解現有格式的格式，請按一 [!UICONTROL Formats] 下功能表列中的選項，然後依名稱或ID號碼搜尋格式。 格式中使用的格式錯誤或宏將提供格式錯誤的輸出，或將使資訊無法完全輸出。

1. 若要建立新格式，請按一下 **[!UICONTROL Formats]** &gt; **[!UICONTROL Add Format]**。 若要編輯現有格式，請按一下欄中所要的 **[!UICONTROL Name]** 格式。

   ![](assets/create_format.png)

1. 填寫欄位: 
   * **** 名稱：（必要）提供格式的描述性名稱。
   * **** 類型：（必要）選擇所要的格式：
      * **[!UICONTROL File]**:透過檔案傳送 [!DNL FTP] 資料。
      * **[!UICONTROL HTTP]**:將資料封裝在包裝 [!DNL JSON] 函式中。

1. （條件性）如果您選 **[!UICONTROL File]**&#x200B;擇，請填寫下列欄位：

   >[!NOTE]
   >
   >有關可用宏的清單，請參 [閱檔案格式宏](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089)[和HTTP格式宏](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE)。

   * **[!UICONTROL File Name]** :指定資料傳輸檔案的檔案名稱。
   * **** 頁首：指定資料傳輸檔案第一行中顯示的文字。
   * **[!UICONTROL Data Row]** :指定出現在檔案每個外界列中的文字。
   * **[!UICONTROL Maximum File Size (In MB)]** :指定資料傳輸檔案的檔案大小上限。 壓縮檔案必須小於100 MB。 未壓縮的檔案大小沒有限制。
   * **[!UICONTROL Compression]** :選擇所需的壓縮類型：gz或zip。 若要傳送 [!UICONTROL AWS S3]至，您必須使用。gz或解壓縮檔案。
   * **[!UICONTROL .info Receipt]** :指定生成轉移控制([!DNL .info])檔案。 檔案 [!DNL .info] 提供檔案傳輸的中繼資料資訊，讓合作夥伴可確認Audience manager已正確處理檔案傳輸。 有關詳細資訊，請 [參閱日誌檔案傳輸的傳輸控制檔案](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html)。
   * **[!UICONTROL MD5 Checksum Receipt]** :指定生成 [!DNL MD5] 校驗和接收。 校驗 [!DNL MD5] 總和收據，讓合作夥伴可以確認Audience manager已正確處理完整傳輸。

1. （條件性）如果您選 **[!UICONTROL HTTP]**&#x200B;擇，請填寫下列欄位：

   * **[!UICONTROL Method]** :選擇要 [!DNL API] 用於轉移流程的方法：
      * **[!UICONTROL POST]** :如果您選 [!DNL POST]取，請選取內容類型([!DNL XML] 或 [!DNL JSON])，然後指定請求內文。
      * **[!UICONTROL GET]** :如果選擇 [!DNL GET]，請指定查詢參數。

1. 如果 **[!UICONTROL Create]** 要建立新格式，請按一下，或者如果 **[!UICONTROL Save Updates]** 要編輯現有格式，請按一下。

## 刪除格式 {#delete-format}

1. Click **[!UICONTROL Formats]**.
2. 按一 ![](assets/icon_delete.png) 下所 **[!UICONTROL Actions]** 要格式的欄。
3. Click **[!UICONTROL OK]** to confirm the deletion.
