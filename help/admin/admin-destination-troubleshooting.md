---
description: 可協助您在Audience Manager中設定目的地並避免常見問題的資訊。
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

可協助您在Audience Manager中設定目的地並避免常見問題的資訊。

## 我設定了目的地，但看不到任何檔案。 它們在哪裡？ {#destination-no-files}

<!-- c_dest_tshooting.xml -->

常見的目的地設定問題包括下列問題：

### 設定錯誤的目的地

* **不正確 [!UICONTROL UserID] 索引鍵：** 此 [!UICONTROL UserID] 索引鍵是 [!UICONTROL MasterDPID] ，也是將上傳ID值的基礎。 即使 [!UICONTROL UserID] 索引鍵可透過下拉式清單選取，並不一定表示有對應至此值的ID/特徵/區段。 如果 [!UICONTROL Outbound] 處理程式（會在建立目的地之後執行）找不到任何對應至此的使用者 [!UICONTROL UserID] 機碼，不會傳回任何資料。
* **未選取檔案資料來源中的：** 當選擇任何目的地型別時 [!UICONTROL S2S]，畫面底部會出現一個區段，標籤為 [!UICONTROL Configure Data Sources]. 此區段首次出現時，不會選取任何值。 如果您忘記按一下 [!UICONTROL All First Party] 核取方塊，或個別選取資料來源 [!UICONTROL Available Data Sources] 視窗中，不會傳回任何資料。

### 格式設定錯誤

為輸出資料選取格式時，如果可能的話，最好重複使用現有格式。 使用已被證實的格式可確保成功產生您的傳出資料。 若要檢視現有格式的確切格式，請按一下 [!UICONTROL Formats] 選單列中的選項，並依名稱或ID編號搜尋您的格式。 格式錯誤的格式或格式中使用的巨集將提供格式不正確的輸出，或阻止完全輸出資訊。

如需設定格式和使用巨集的詳細資訊，請參閱 [檔案格式巨集](formats/file-formats.md#) 和 [http格式巨集](formats/web-formats.md).

### 設定錯誤的伺服器

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 請勿輸入主機名稱的前置詞。 如果您有指定的帳戶 [!DNL ftp://hello.com]，直接輸入 [!DNL hello.com] 在此欄位中。
   * **[!UICONTROL Port/Type Combination]**
      * 對於 [!DNL FTP] 轉移，首選轉移型別為 [!DNL SFTP].
      * 選取 [!DNL SFTP] 型別，連線埠幾乎總是22。
      * 選取 [!DNL FTPs/TLS] 型別，連線埠幾乎總是21。
      * 此 [!DNL FTPs/TLS] 型別與一般型別不同 [!DNL FTP] 轉移。 我們不支援定期（不安全） [!DNL FTP] 傳輸。
   * **[!UICONTROL Remote Path]**
      * 選擇遠端子路徑時，輸入時不應使用前導斜線。
      * 如果您要傳送的檔案應放在 [!DNL (root)/inbound] 子資料夾，直接新增 [!DNL inbound] 遠端路徑，而非 [!DNL /inbound].
      * 如果沿路徑將檔案傳送至多個目錄，請在每個目錄之間輸入斜線。 如果您被指定位置 [!DNL /inbound/subdirectory1/subdirectory2]，請輸入 [!DNL inbound/subdirectory1/subdirectory2] 在此欄位中。
      * 如果檔案應放置在外部伺服器自動路由到的目錄中，您可以將此空間留空。 請勿輸入句點( 。 )、斜線( / )或任何其他專案。

* **[!DNL S3]**
   * [!DNL S3] 是偏好的傳輸通訊協定(超過 [!DNL FTP] 或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 儲存貯體名稱應該列出時不含斜線、首碼、尾碼等。 如果您有指定的地址 [!DNL s3://your-bucket] 您只需新增 [!DNL your-bucket] 至此欄位。
      * **[!UICONTROL Directory]**
         * 除非您特別指定要將資料放置到的子目錄，否則請將此欄位留空。 如果您有指定的地址 [!DNL s3://your-bucket/your-subdirectory]，輸入 [!DNL your-bucket] 在 [!UICONTROL Bucket] 欄位和 [!DNL your-subdirectory] 應已新增至 [!UICONTROL Directory] 欄位。 請勿新增前面的斜線。
         * 如果您必須沿著路徑瀏覽多個目錄，則只有使用斜線作為分隔符號時。 因此， [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 會有 [!DNL your-bucket] 在 [!UICONTROL Bucket] 欄位和 [!DNL your-subdirectory1/your-subdirectory2] 已輸入 [!UICONTROL Directory] 欄位。
      * **[!UICONTROL Access / Secret Keys]**
         * 時間 [!DNL TechOps] 建立儲存貯體並向顧問提供存取/秘密金鑰，這些憑證通常是 `READ-ONLY` 本該傳遞給使用者端的認證。 這些認證不應輸入至 [!UICONTROL Access / Secret Key] 欄位，因為這會造成傳輸失敗（因為這些認證是唯讀的，無法寫入）。 在 [!DNL TechOps] 建立儲存貯體並提供認證，顧問也應請求Adobe金鑰組（不要提供給使用者端）以允許將檔案寫入此儲存貯體。 應該將該索引鍵新增到這些欄位中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 請輸入「 」的前置詞資訊 [!DNL HTTP] 個專案。 如果您有指定的帳戶 [!DNL https://superduper.com]，輸入 [!DNL https://superduper.com] 在此欄位中。
      * **[!UICONTROL URL Prefix]**
         * 新增 [!DNL URL] 前置詞，將前面的斜線保持關閉。 位址 [!DNL https://hello.com/r/x/y/z] 應該有 [!DNL https://hello.com] 輸入於 [!UICONTROL Domain] 欄位和 [!DNL r/x/y/z] 在此輸入於 [!UICONTROL URL Prefix] 欄位。
         * 若為 [!UICONTROL URL Prefix] 不需要，請將此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 輸入完整的 `SSH PRIVATE` 此方塊中的金鑰值（包括頁首、頁尾和分行符號）可確保加密或金鑰儲存準確無誤。

### 沒有足夠的時間產生輸出

展開程式每天執行兩次，並會執行多個程式（展開、發佈、推送至外部位置等） 必須先執行，檔案才會推送至其最終目的地。 一個好的經驗法則是，目的地應於至少24小時前完成完整設定，才可將資料推送至外部位置。

### 檔案分割大小太大

將檔案外送至目的地時，您可以在檔案區塊中分割較大的外送檔案。 請確定個別檔案區塊不超過10 GB。 另請參閱 [傳出資料檔案名稱：語法和範例](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## 如何設定目的地，以匯出資料檔案中的Experience CloudID、客戶ID或Audience ManagerID {#set-up-destinations-export}

此頁面說明如何設定目的地，以匯出以您要的ID型別作為輸入資料的目的地 [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

目的地可讓我們的客戶在任意數量的數位頻道上啟用其資料。 例如，他們可以將受眾資料匯出至其他 [!DNL Adobe Experience Cloud] 解決方案([!DNL Target]， [!DNL Campaign]、等)。 或者，他們也可以將資料傳送至 [!UICONTROL DSP]s， [!UICONTROL SSP]s或任何與Audience Manager整合的平台。 我們會保留一份與合作的合作夥伴清單 [整合Wiki頁面](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>如需在管理員UI中建立目的地的詳細逐步解說，請檢視 [建立或編輯公司目的地](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 文章。

您的客戶想要根據目的地匯出不同的ID型別。 以下組態圖表顯示您應該選取哪些選項來匯出與不同ID型別相關的設定檔資訊。 建議您也參閱 [Audience Manager內的ID索引](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). 有三個重要的設定需要考慮： [!UICONTROL User ID Key]，則 [!UICONTROL Data Source Type] 和 [!UICONTROL Format]. 我們將在下方詳細介紹所有這些功能。

* [!UICONTROL User ID Key]。在 [!UICONTROL Admin UI]，前往 **[!UICONTROL Companies]**. 搜尋您的客戶公司並按一下它。 尋找 **[!UICONTROL Destinations]** tab鍵並按下 **[!UICONTROL Add Destination]**. 在 **[!UICONTROL Add Destination]** 工作流程，選取 [!UICONTROL User ID Key]. 此 [!UICONTROL User ID Key] 會篩選來自目標資料來源的傳入ID，並僅允許ID通過。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience ManagerUI中建立目的地時選取此選項。 首先，選取 [!UICONTROL Inbound]，然後選取您想要的ID型別。 選項包括：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此選項會決定要匯出的檔案格式。 在 **[!UICONTROL Add Destination]** 工作流程，在 **[!UICONTROL Batch Data]**，選取格式。

若要檢查格式，請前往 **[!UICONTROL Admin UI > Formats]** 並尋找 [!UICONTROL Data Row] 元素。 此元素包含檔案格式的巨集， &lt;mcid> 在以下範例中。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 設定編號 </th> 
   <th colname="col1" class="entry"> <p>使用者金鑰 </p> </th> 
   <th colname="col2" class="entry"> <p>資料來源型別 </p> </th> 
   <th colname="col3" class="entry"> <p>格式 </p> </th> 
   <th colname="col4" class="entry"> <p>匯出的ID型別 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID （公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>客戶ID (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID （公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID （公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID （公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID （公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID （公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用個案

假設您使用Audience Manager和 [!DNL Campaign]. 為了讓客戶資料在中可操作 [!DNL Campaign]，您想要匯出 [!UICONTROL Experience Cloud IDs]. 在這種情況下，您應該使用設定編號3。
