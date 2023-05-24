---
description: 使用「Audience Manager管理工具」中的「格式」頁面來建立新格式或編輯現有格式。
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: 建立或編輯格式
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 3%

---

# 建立或編輯格式 {#create-or-edit-a-format}

使用 [!UICONTROL Formats] 頁面，以建立新格式或編輯現有Audience Manager格式。

<!-- t_create_format.xml -->

>[!TIP]
>
>為輸出資料選取格式時，如果可能的話，最好重複使用現有格式。 使用已被證實的格式可確保成功產生您的傳出資料。 若要檢視現有格式的確切格式，請按一下 [!UICONTROL Formats] 選單列中的選項，並依名稱或ID編號搜尋您的格式。 格式錯誤的格式或格式中使用的巨集將提供格式不正確的輸出，或阻止完全輸出資訊。

1. 若要建立新格式，請按一下 **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. 若要編輯現有格式，請在 **[!UICONTROL Name]** 欄。

   ![](assets/create_format.png)

1. 填寫欄位: 
   * **名稱：** （必要）提供格式的描述性名稱。
   * **型別：** （必要）選取所需的格式：
      * **[!UICONTROL File]**：透過傳送資料 [!DNL FTP] 檔案。
      * **[!UICONTROL HTTP]**：將資料內嵌於 [!DNL JSON] 包裝函式。

1. （視條件而定）如果您選擇 **[!UICONTROL File]**，填寫欄位：

   >[!NOTE]
   >
   >如需可用巨集的清單，請參閱 [檔案格式巨集](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) 和 [http格式巨集](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]：** 指定資料傳輸檔案的檔案名稱。
   * **頁首：** 指定出現在資料傳輸檔案第一列的文字。
   * **[!UICONTROL Data Row]：** 指定顯示在檔案之每個展開列中的文字。
   * **[!UICONTROL Maximum File Size (In MB)]：** 指定資料傳輸檔案的檔案大小上限。 壓縮檔案必須小於100 MB。 未壓縮檔案大小沒有限制。
   * **[!UICONTROL Compression]：** 為您的資料檔案選取所需的壓縮型別：gz或zip。 針對傳遞至 [!UICONTROL AWS S3]，您必須使用.gz或未壓縮的檔案。
   * **[!UICONTROL .info Receipt]：** 指定傳輸控制([!DNL .info])檔案產生。 此 [!DNL .info] file提供有關檔案傳輸的中繼資料資訊，以便合作夥伴可以驗證Audience Manager是否正確處理檔案傳輸。 如需詳細資訊，請參閱 [用於記錄檔傳輸的傳輸控制檔案](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en).
   * **[!UICONTROL MD5 Checksum Receipt]：** 指定 [!DNL MD5] 已產生總和檢查碼回條。 此 [!DNL MD5] 總和檢查碼回執，讓合作夥伴可驗證Audience Manager是否正確處理完整傳輸。

1. （視條件而定）如果您選擇 **[!UICONTROL HTTP]**，填寫欄位：

   * **[!UICONTROL Method]：** 選擇 [!DNL API] 您要用於傳輸處理的方法：
      * **[!UICONTROL POST]：** 如果您選取 [!DNL POST]，選取內容型別([!DNL XML] 或 [!DNL JSON])，然後指定要求內文。
      * **[!UICONTROL GET]：** 如果您選取 [!DNL GET]，指定查詢引數。

1. 按一下 **[!UICONTROL Create]** 如果您要建立新格式，或按一下 **[!UICONTROL Save Updates]** 如果您正在編輯現有格式。

## 刪除格式 {#delete-format}

1. 按一下 **[!UICONTROL Formats]**.
2. 按一下  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 欄中指定的格式。
3. 按一下 **[!UICONTROL OK]** 以確認刪除。
