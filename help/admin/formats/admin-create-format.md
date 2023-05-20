---
description: 使用「Audience Manager管理」工具中的「格式」頁可建立新格式或編輯現有格式。
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

使用 [!UICONTROL Formats] 的子菜單。

<!-- t_create_format.xml -->

>[!TIP]
>
>為外界資料選擇格式時，最好（如果可能）重新使用現有格式。 使用已驗證的格式可確保成功生成出站資料。 要確切瞭解現有格式的格式，請按一下 [!UICONTROL Formats] 的子菜單。 格式不正確或格式中使用的宏將提供格式不正確的輸出，或將阻止完全輸出資訊。

1. 要建立新格式，請按一下 **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**。 要編輯現有格式，請在 **[!UICONTROL Name]** 的雙曲餘切值。

   ![](assets/create_format.png)

1. 填寫欄位: 
   * **名稱：** （必需）提供格式的描述性名稱。
   * **類型：** （必需）選擇所需格式：
      * **[!UICONTROL File]**:通過 [!DNL FTP] 的子菜單。
      * **[!UICONTROL HTTP]**:將資料封裝在 [!DNL JSON] 包裝。

1. （條件）如果您選擇 **[!UICONTROL File]**，填寫欄位：

   >[!NOTE]
   >
   >有關可用宏的清單，請參見 [檔案格式宏](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) 和 [HTTP格式宏](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE)。

   * **[!UICONTROL File Name]:** 指定資料傳輸檔案的檔案名。
   * **標題：** 指定資料傳輸檔案第一行中顯示的文本。
   * **[!UICONTROL Data Row]:** 指定檔案的每行外界顯示的文本。
   * **[!UICONTROL Maximum File Size (In MB)]:** 指定資料傳輸檔案的最大檔案大小。 壓縮檔案必須小於100 MB。 未壓縮檔案大小沒有限制。
   * **[!UICONTROL Compression]:** 選擇所需的壓縮類型：gz或zip。 用於交貨到 [!UICONTROL AWS S3]，必須使用.gz或未壓縮檔案。
   * **[!UICONTROL .info Receipt]:** 指定轉移控制([!DNL .info])檔案。 的 [!DNL .info] file提供了有關檔案傳輸的元資料資訊，以便合作夥伴可以驗證Audience Manager處理的檔案傳輸是否正確。 有關詳細資訊，請參見 [日誌檔案傳輸的傳輸控制檔案](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en)。
   * **[!UICONTROL MD5 Checksum Receipt]:** 指定 [!DNL MD5] 生成校驗和接收。 的 [!DNL MD5] 校驗和接收，以便合作夥伴可以驗證Audience Manager是否正確處理完全傳輸。

1. （條件）如果您選擇 **[!UICONTROL HTTP]**，填寫欄位：

   * **[!UICONTROL Method]:** 選擇 [!DNL API] 用於轉移流程的方法：
      * **[!UICONTROL POST]:** 如果選擇 [!DNL POST]，選擇內容類型([!DNL XML] 或 [!DNL JSON])，然後指定請求正文。
      * **[!UICONTROL GET]:** 如果選擇 [!DNL GET]，指定查詢參數。

1. 按一下 **[!UICONTROL Create]** 建立新格式時，按一下 **[!UICONTROL Save Updates]** 的子菜單。

## 刪除格式 {#delete-format}

1. 按一下 **[!UICONTROL Formats]**.
2. 按一下  ![](assets/icon_delete.png) 的 **[!UICONTROL Actions]** 的子菜單。
3. 按一下 **[!UICONTROL OK]** 確認刪除。
