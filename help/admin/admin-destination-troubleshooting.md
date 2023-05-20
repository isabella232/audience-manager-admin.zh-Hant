---
description: 幫助您設定Audience Manager目標並避免常見問題的資訊。
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: 目的地設定疑難排解
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# 目的地設定疑難排解 {#destination-setup-troubleshooting}

幫助您設定Audience Manager目標並避免常見問題的資訊。

## 我設定了目標，但沒看到任何檔案。 它們在哪裡？ {#destination-no-files}

<!-- c_dest_tshooting.xml -->

常見目標配置問題包括以下問題：

### 目標配置錯誤

* **錯誤 [!UICONTROL UserID] 鍵：** 的 [!UICONTROL UserID] 鍵 [!UICONTROL MasterDPID] 的ID值。 即使 [!UICONTROL UserID] 通過下拉清單可選擇鍵，但不一定意味著有ID/traits/segment映射到此值。 如果 [!UICONTROL Outbound] 進程（在建立目標後運行）找不到映射到此的任何用戶 [!UICONTROL UserID] 鍵，任何資料都不會被超出界限。
* **未選擇檔案資料源：** 選擇除 [!UICONTROL S2S]，螢幕底部將顯示一個標有 [!UICONTROL Configure Data Sources]。 首次顯示此節時，不會選擇任何值。 如果忘記按一下 [!UICONTROL All First Party] 複選框，或單獨從 [!UICONTROL Available Data Sources] 窗口，任何資料都不會被超限。

### 格式配置錯誤

為外界資料選擇格式時，最好（如果可能）重新使用現有格式。 使用已驗證的格式可確保成功生成出站資料。 要確切瞭解現有格式的格式，請按一下 [!UICONTROL Formats] 的子菜單。 格式不正確或格式中使用的宏將提供格式不正確的輸出，或將阻止完全輸出資訊。

有關設定格式和使用宏的詳細資訊，請參見 [檔案格式宏](formats/file-formats.md#) 和 [HTTP格式宏](formats/web-formats.md)。

### 伺服器配置錯誤

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 請勿輸入主機名的任何前置詞。 如果你有賬戶 [!DNL ftp://hello.com]，按一下 [!DNL hello.com] 的子菜單。
   * **[!UICONTROL Port/Type Combination]**
      * 對於 [!DNL FTP] 傳輸，首選傳輸類型為 [!DNL SFTP]。
      * 選擇 [!DNL SFTP] 類型，埠幾乎總是22。
      * 選擇 [!DNL FTPs/TLS] 類型，埠幾乎總是21。
      * 的 [!DNL FTPs/TLS] 類型與常規類型不同 [!DNL FTP] 轉移。 我們不支援常規（無擔保） [!DNL FTP] 轉移。
   * **[!UICONTROL Remote Path]**
      * 選擇遠程子路徑時，應輸入該路徑時不帶前導斜槓。
      * 如果傳輸的檔案應放在 [!DNL (root)/inbound] 子資料夾，只需添加 [!DNL inbound] 遠程路徑，而不是 [!DNL /inbound]。
      * 如果在路徑中發送檔案多個目錄，請在每個目錄之間輸入斜槓。 如果你知道 [!DNL /inbound/subdirectory1/subdirectory2]，您應輸入 [!DNL inbound/subdirectory1/subdirectory2] 的子菜單。
      * 如果檔案應放在外部伺服器自動路由到的目錄中，則可將此空間留空。 不輸入期間(. )、斜槓(/)或其它任何選項。

* **[!DNL S3]**
   * [!DNL S3] 是首選傳輸協定(通過 [!DNL FTP] 或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 儲存段名稱應列出，不應包含斜槓、前置詞、尾碼等。 如果你有地址 [!DNL s3://your-bucket] 您只需添加 [!DNL your-bucket] 到此欄位。
      * **[!UICONTROL Directory]**
         * 將此欄位留空，除非您特別指定了一個子目錄，資料應放在該子目錄中。 如果你有地址 [!DNL s3://your-bucket/your-subdirectory]輸入 [!DNL your-bucket] 的 [!UICONTROL Bucket] 欄位和 [!DNL your-subdirectory] 應該被添加到 [!UICONTROL Directory] 的子菜單。 不要添加前面的斜槓。
         * 如果必須沿路徑傳輸多個目錄，則只應使用斜槓作為分隔符。 所以一個 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 會 [!DNL your-bucket] 的 [!UICONTROL Bucket] 欄位和 [!DNL your-subdirectory1/your-subdirectory2] 的 [!UICONTROL Directory] 的子菜單。
      * **[!UICONTROL Access / Secret Keys]**
         * 當 [!DNL TechOps] 建立儲存桶並為顧問提供訪問/密鑰，這些憑據通常 `READ-ONLY` 本該交給客戶的憑據。 不應將這些憑據輸入到 [!UICONTROL Access / Secret Key] 欄位，因為這將導致傳輸失敗（因為這些憑據是只讀的，不可寫）。 如果 [!DNL TechOps] 建立儲存桶並提供憑據，顧問還應請求一個Adobe密鑰對，以允許將檔案寫入此儲存桶。 該密鑰應添加到這些欄位中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 輸入前置詞資訊 [!DNL HTTP] 的子菜單。 如果你有賬戶 [!DNL https://superduper.com]輸入 [!DNL https://superduper.com] 的子菜單。
      * **[!UICONTROL URL Prefix]**
         * 添加 [!DNL URL] 前置詞，將前面的斜槓撇開。 地址 [!DNL https://hello.com/r/x/y/z] 應該 [!DNL https://hello.com] 的 [!UICONTROL Domain] 欄位和 [!DNL r/x/y/z] 輸入 [!UICONTROL URL Prefix] 的子菜單。
         * 如果 [!UICONTROL URL Prefix] 不需要，請將此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 輸入完整 `SSH PRIVATE` 框中的鍵值，包括頁眉、頁腳和換行符，以確保準確的加密/密鑰儲存。

### 出站生成時間不足

外部進程每天運行兩次，並且運行多個進程（外部、發佈、推送到外部位置等） 必須在將檔案推送到其最終目標之前運行。 一個很好的經驗法則是，在將資料推送到外部位置之前，應至少在24小時內對目標進行完全配置。

### 檔案拆分大小過大

將檔案外部定界到目標時，可以將較大的出站檔案以檔案塊形式拆分。 確保單個檔案塊不超過10 GB。 另請參見 [出站資料檔案名：語法和示例](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en)。


## 如何設定目標以導出出站資料檔案中的Experience CloudID、客戶ID或Audience ManagerID {#set-up-destinations-export}

此頁顯示如何設定目標以導出與所需ID類型鎖定的資料 [!UICONTROL Outbound Data Files]。

<!-- set-up-destinations-mcid-aamid.xml -->

目的地允許我們的客戶通過任意數量的數字通道激活其資料。 例如，他們可以將受眾資料導出到其他 [!DNL Adobe Experience Cloud] 解決方案([!DNL Target]。 [!DNL Campaign]等)。 或者，他們可以發送資料 [!UICONTROL DSP]s [!UICONTROL SSP]或與Audience Manager整合的任何平台。 我們有一份合作夥伴名單 [整合Wiki頁](https://wiki.corp.adobe.com/display/MCPI)。

>[!NOTE]
>
>有關在管理員UI中建立目標的詳細步驟，請參閱 [建立或編輯公司目標](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 文章。

您的客戶希望導出不同的ID類型，具體取決於目標。 下面的配置圖顯示了應選擇的選項，以導出與不同ID類型相關的配置檔案資訊。 我們建議您也參考 [Audience Manager中ID的索引](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en)。 有三個重要設定需要考慮， [!UICONTROL User ID Key]，也請參見Wiki頁。 [!UICONTROL Data Source Type] 和 [!UICONTROL Format]。 我們詳細記錄下面所有的細節。

* [!UICONTROL User ID Key]。在 [!UICONTROL Admin UI]，轉到 **[!UICONTROL Companies]**。 搜索客戶的公司，然後按一下。 查找 **[!UICONTROL Destinations]** 按 **[!UICONTROL Add Destination]**。 在 **[!UICONTROL Add Destination]** 工作流，選擇 [!UICONTROL User ID Key]。 的 [!UICONTROL User ID Key] 將過濾目標資料源中的傳入ID，並僅允許ID通過。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience ManagerUI中建立目標時選擇此選項。 首先，選擇 [!UICONTROL Inbound]，然後選擇所需的ID類型。 選項包括：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此選項確定要導出的檔案格式。 在 **[!UICONTROL Add Destination]** 工作流，下 **[!UICONTROL Batch Data]**&#x200B;的雙曲餘切值。

要檢查格式，請轉到 **[!UICONTROL Admin UI > Formats]** 尋找 [!UICONTROL Data Row] 的子菜單。 此元素包含檔案格式的宏， &lt;mcid> 中。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 配置編號 </th> 
   <th colname="col1" class="entry"> <p>用戶密鑰 </p> </th> 
   <th colname="col2" class="entry"> <p>資料源類型 </p> </th> 
   <th colname="col3" class="entry"> <p>格式 </p> </th> 
   <th colname="col4" class="entry"> <p>導出的ID類型 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID（公司有權訪問的任何資料源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>客戶ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID（公司有權訪問的任何資料源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID（公司有權訪問的任何資料源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID（公司有權訪問的任何資料源） </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID（公司有權訪問的任何資料源） </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID（公司有權訪問的任何資料源） </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用個案

假設你用Audience Manager [!DNL Campaign]。 為了使客戶資料在 [!DNL Campaign]，您要導出 [!UICONTROL Experience Cloud IDs]。 在這種情況下，應使用配置編號3。
