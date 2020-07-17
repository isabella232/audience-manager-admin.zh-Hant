---
description: 這些資訊可協助您在Audience Manager中設定目標，並避免常見問題。
seo-description: 這些資訊可協助您在Audience Manager中設定目標，並避免常見問題。
seo-title: 目的地設定疑難排解
title: 目的地設定疑難排解
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 4%

---


# 目的地設定疑難排解{#destination-setup-troubleshooting}

這些資訊可協助您在Audience Manager中設定目標，並避免常見問題。

## 我設定了目的地，但我沒看到任何檔案。 它們在哪裡？{#destination-no-files}

<!-- c_dest_tshooting.xml -->

常見的目標配置問題包括以下問題：

### 目標配置錯誤

* **密[!UICONTROL UserID]鑰不正確：** 鍵 [!UICONTROL UserID] 是此目 [!UICONTROL MasterDPID] 的地的，是ID值將被超出界的基礎。 即使透過 [!UICONTROL UserID] 下拉式清單可選取索引鍵，也不一定表示有ID/特徵／區段對應至此值。 如果進 [!UICONTROL Outbound] 程（在建立目標後執行）找不到任何對應至此索引鍵的使用者， [!UICONTROL UserID] 則不會有任何資料超出界限。
* **未在檔案資料來源中選取：** 當選擇除外的任何目標類 [!UICONTROL S2S]型時，會在標有標籤的畫面底部顯示區段 [!UICONTROL Configure Data Sources]。 首次出現此部分時，不會選擇任何值。 如果您忘記按一下核取方 [!UICONTROL All First Party] 塊或從視窗個別選取資料來源，則 [!UICONTROL Available Data Sources] 不會有任何資料超出界限。

### 配置錯誤的格式

為外界資料選擇格式時，最好盡可能重新使用現有格式。 使用已證實可行的格式，可確保您的傳出資料能成功產生。 若要確切瞭解現有格式的格式，請按一 [!UICONTROL Formats] 下功能表列中的選項，然後依名稱或ID號碼搜尋格式。 格式中使用的格式錯誤或宏將提供格式錯誤的輸出，或將使資訊無法完全輸出。

有關設定格式和使用宏的詳細資訊，請參 [閱檔案格式宏](formats/file-formats.md#)[和HTTP格式宏](formats/web-formats.md)。

### 伺服器配置錯誤

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 請勿為主機名輸入任何前置詞。 如果您有帳戶，只 [!DNL ftp://hello.com]要在此欄 [!DNL hello.com] 位中輸入。
   * **[!UICONTROL Port/Type Combination]**
      * 對於轉 [!DNL FTP] 讓，優選的轉讓類型是 [!DNL SFTP]。
      * 在選擇類 [!DNL SFTP] 型時，埠幾乎總是22。
      * 在選擇類 [!DNL FTPs/TLS] 型時，埠幾乎總是21。
      * 類 [!DNL FTPs/TLS] 型與常規傳輸不同 [!DNL FTP] 。 我們不支援定期（無擔保）轉 [!DNL FTP] 讓。
   * **[!UICONTROL Remote Path]**
      * 選擇遠程子路徑時，應使用無前導斜線輸入該路徑。
      * 如果傳輸的檔案應放在子資料夾中， [!DNL (root)/inbound] 只需為遠程路 [!DNL inbound] 徑添加，不要 [!DNL /inbound]。
      * 如果沿路徑發送檔案多個目錄，請在每個目錄之間輸入斜線。 如果給出的位置 [!DNL /inbound/subdirectory1/subdirectory2]，則應在此字 [!DNL inbound/subdirectory1/subdirectory2] 段中輸入。
      * 如果您的檔案應放置在外部伺服器自動路由至的目錄中，您可將此空格留空。 請勿輸入期間(. )、斜線(/)或其他任何項目。

* **[!DNL S3]**
   * [!DNL S3] 是首選的傳輸協定( [!DNL FTP] over或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 貯體名稱應列在清單中，不含斜線、前置詞、尾碼等。 如果您獲得地址， [!DNL s3://your-bucket] 您只需將其 [!DNL your-bucket] 添加到此欄位。
      * **[!UICONTROL Directory]**
         * 請將此欄位留空，除非您特別給出了應將資料放入的子目錄。 如果您已獲得地址 [!DNL s3://your-bucket/your-subdirectory]，請在字 [!DNL your-bucket] 段中 [!UICONTROL Bucket] 輸入， [!DNL your-subdirectory] 並應將其添加到 [!UICONTROL Directory] 欄位中。 不要添加前面的斜線。
         * 如果必須沿路徑傳送多個目錄，則只應使用斜線作為分隔符。 因此，某個位 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 置會 [!DNL your-bucket] 在欄位中 [!UICONTROL Bucket] 並 [!DNL your-subdirectory1/your-subdirectory2] 輸入到 [!UICONTROL Directory] 欄位。
      * **[!UICONTROL Access / Secret Keys]**
         * 當建 [!DNL TechOps] 立儲存貯體並提供存取／機密金鑰給顧問時，這些憑證通常是 `READ-ONLY` 要交給用戶端的憑證。 這些憑據不應輸入到字 [!UICONTROL Access / Secret Key] 段中，因為這會導致傳輸失敗（因為這些憑據是只讀的，不可寫的）。 如果建立儲 [!DNL TechOps] 存貯體並提供認證，顧問也應要求Adobe金鑰對——不要提供給用戶端——允許將檔案寫入此儲存貯體。 應將該鍵添加到這些欄位中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 請輸入條目的前置詞 [!DNL HTTP] 資訊。 如果您有帳戶，請 [!DNL https://superduper.com]在此欄 [!DNL https://superduper.com] 位中輸入。
      * **[!UICONTROL URL Prefix]**
         * 新增前置詞 [!DNL URL] 時，請將前面的斜線保留為off。 應已在字 [!DNL https://hello.com/r/x/y/z] 段中輸 [!DNL https://hello.com] 入地址， [!UICONTROL Domain] 並在 [!DNL r/x/y/z] 此欄位中輸入 [!UICONTROL URL Prefix] 地址。
         * 如果不 [!UICONTROL URL Prefix] 需要，請將此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 在此方塊中 `SSH PRIVATE` 輸入完整的金鑰值，包括頁首、頁尾和分行符號，以確保正確的加密／金鑰儲存。

### 外發時間不足

外框程式每天執行兩次，而且有多個程式（外框、發佈、推送至外部位置等） 必須在檔案推送至其最終目的地之前執行。 一個很好的經驗法則是，目標應至少在24小時內完全配置，您才能預期資料會推送至外部位置。

### 檔案分割大小過大

當將檔案外框至目的地時，您可以將較大的外框檔案分割為檔案區塊。 請確定個別檔案區塊不超過10 GB。 See also, [Outbound Data File Name: Syntax and Examples](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## 如何設定目標，將Experience Cloud ID、客戶ID或Audience Manager ID匯出至傳出資料檔案 {#set-up-destinations-export}

This page shows you how to set up destinations to export data keyed off the ID type you want in [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

目標可讓客戶透過任何數位通道啟動其資料。 例如，他們可以將觀眾資料匯出至其 [!DNL Adobe Experience Cloud] 他解決方案[!DNL Target]( [!DNL Campaign]、等等)。 或者，他們可以傳送資 [!UICONTROL DSP]料至s [!UICONTROL SSP]、s或任何與Audience Manager整合的平台。 我們在「整合Wiki」頁面上保留與我們合作 [的合作夥伴清單](https://wiki.corp.adobe.com/display/MCPI)。

>[!NOTE]
>
>如需有關在管理員UI中建立目標的詳細逐步說明，請參閱「建立或編 [輯公司目標」文章](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 。

您的客戶想要匯出不同的ID類型，視目標而定。 下面的配置圖表顯示了應選擇哪些選項，以導出與不同ID類型相關的配置檔案資訊。 我們建議您也參考Audience Manager [中的ID索引](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)。 有三個重要的設定要考 [!UICONTROL User ID Key]慮， [!UICONTROL Data Source Type] 即、和 [!UICONTROL Format]。 我們詳細說明下面的所有細節。

* [!UICONTROL User ID Key]。在中 [!UICONTROL Admin UI]，轉到 **[!UICONTROL Companies]**。 搜尋客戶的公司，然後按一下。 查找標 **[!UICONTROL Destinations]** 簽並按 **[!UICONTROL Add Destination]**。 在工作 **[!UICONTROL Add Destination]** 流中，選擇 [!UICONTROL User ID Key]。 The [!UICONTROL User ID Key] will filter the inming IDs from the target data source and only allow the IDs to pass.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience Manager UI中建立目標時，請選取此選項。 首先，選擇 [!UICONTROL Inbound]，然後選擇所需的ID類型。 選項包括：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此選項決定您要匯出的檔案格式。 在工作流 **[!UICONTROL Add Destination]** 的下方， **[!UICONTROL Batch Data]**&#x200B;選擇格式。

若要檢查格式，請前 **[!UICONTROL Admin UI > Formats]** 往並尋找元 [!UICONTROL Data Row] 素。 此元素包含檔案格式的巨集，&lt;MCID>如下例所示。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 配置號。 </th> 
   <th colname="col1" class="entry"> <p>使用者金鑰 </p> </th> 
   <th colname="col2" class="entry"> <p>資料來源類型 </p> </th> 
   <th colname="col3" class="entry"> <p>格式 </p> </th> 
   <th colname="col4" class="entry"> <p>匯出的ID類型 </p> </th> 
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
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
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
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>客戶ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用個案

假設您使用Audience Manager和 [!DNL Campaign]。 為了讓客戶資料在中可操作， [!DNL Campaign]您需要匯出 [!UICONTROL Experience Cloud IDs]。 在這種情況下，應使用配置編號3。