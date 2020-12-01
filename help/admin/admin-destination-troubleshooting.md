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

* **不正 [!UICONTROL UserID] 確的** 鍵： [!UICONTROL UserID] 鍵是 [!UICONTROL MasterDPID] 此目的地的基礎，是ID值將被超出界的基礎。即使[!UICONTROL UserID]索引鍵可透過下拉式清單選取，也不一定表示有ID/特徵／區段已對應至此值。 如果[!UICONTROL Outbound]進程（在建立目標後運行）找不到映射到此[!UICONTROL UserID]鍵的任何用戶，則不會有任何資料被超界。
* **未選取檔案中的資料來源：** 選擇任何目標類型以外的 [!UICONTROL S2S]類型時，會在標示為的畫面底部顯示區段 [!UICONTROL Configure Data Sources]。首次出現此部分時，不會選擇任何值。 如果您忘記按一下[!UICONTROL All First Party]核取方塊或從[!UICONTROL Available Data Sources]視窗個別選取資料來源，則不會有任何資料超出界限。

### 配置錯誤的格式

為外界資料選擇格式時，最好盡可能重新使用現有格式。 使用已證實可行的格式，可確保您的傳出資料能成功產生。 要確切瞭解現有格式的格式，請按一下菜單欄中的[!UICONTROL Formats]選項，然後按名稱或ID號搜索格式。 格式中使用的格式錯誤或宏將提供格式錯誤的輸出，或將使資訊無法完全輸出。

有關設定格式和使用宏的詳細資訊，請參閱[檔案格式宏](formats/file-formats.md#)和[HTTP格式宏](formats/web-formats.md)。

### 伺服器配置錯誤

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 請勿為主機名輸入任何前置詞。 如果您有帳戶[!DNL ftp://hello.com]，只需在此欄位中輸入[!DNL hello.com]。
   * **[!UICONTROL Port/Type Combination]**
      * 對於[!DNL FTP]傳輸，首選傳輸類型為[!DNL SFTP]。
      * 選擇[!DNL SFTP]類型時，埠幾乎始終為22。
      * 選擇[!DNL FTPs/TLS]類型時，埠幾乎總是21。
      * [!DNL FTPs/TLS]類型與常規[!DNL FTP]傳輸不同。 我們不支援定期（無擔保）[!DNL FTP]轉讓。
   * **[!UICONTROL Remote Path]**
      * 選擇遠程子路徑時，應使用無前導斜線輸入該路徑。
      * 如果傳輸的檔案應放在[!DNL (root)/inbound]子資料夾中，只需為遠程路徑添加[!DNL inbound]，而不是[!DNL /inbound]。
      * 如果沿路徑發送檔案多個目錄，請在每個目錄之間輸入斜線。 如果您的位置為[!DNL /inbound/subdirectory1/subdirectory2]，則應在此欄位中輸入[!DNL inbound/subdirectory1/subdirectory2]。
      * 如果您的檔案應放置在外部伺服器自動路由至的目錄中，您可將此空格留空。 請勿輸入期間(. )、斜線(/)或其他任何項目。

* **[!DNL S3]**
   * [!DNL S3] 是首選的傳輸協定( [!DNL FTP] over或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 貯體名稱應列在清單中，不含斜線、前置詞、尾碼等。 如果給您地址[!DNL s3://your-bucket]，則只需將[!DNL your-bucket]添加到此欄位。
      * **[!UICONTROL Directory]**
         * 請將此欄位留空，除非您特別給出了應將資料放入的子目錄。 如果給您地址[!DNL s3://your-bucket/your-subdirectory]，請在[!UICONTROL Bucket]欄位中輸入[!DNL your-bucket] ,[!DNL your-subdirectory]應添加到[!UICONTROL Directory]欄位中。 不要添加前面的斜線。
         * 如果必須沿路徑傳送多個目錄，則只應使用斜線作為分隔符。 因此，[!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2]的位置會在[!UICONTROL Bucket]欄位中有[!DNL your-bucket]，而[!DNL your-subdirectory1/your-subdirectory2]則會在[!UICONTROL Directory]欄位中輸入。
      * **[!UICONTROL Access / Secret Keys]**
         * 當[!DNL TechOps]建立儲存貯體並提供存取／密碼金鑰給顧問時，這些憑證通常是`READ-ONLY`憑證，本來是要交給用戶端。 這些憑據不應輸入到[!UICONTROL Access / Secret Key]欄位中，因為這將導致傳輸失敗（因為這些憑據是只讀的，不可寫的）。 當[!DNL TechOps]建立儲存貯體並提供認證時，顧問也應要求Adobe金鑰對——不要提供給用戶端——允許將檔案寫入此儲存貯體。 應將該鍵添加到這些欄位中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 請為[!DNL HTTP]條目輸入前置詞資訊。 如果您有帳戶[!DNL https://superduper.com]，請在此欄位中輸入[!DNL https://superduper.com]。
      * **[!UICONTROL URL Prefix]**
         * 新增[!DNL URL]首碼時，請將前面的斜線保留為off。 [!DNL https://hello.com/r/x/y/z]的地址應在[!UICONTROL Domain]欄位中輸入[!DNL https://hello.com]，並在[!UICONTROL URL Prefix]欄位中輸入[!DNL r/x/y/z]。
         * 如果不需要[!UICONTROL URL Prefix]，請將此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 在此方塊中輸入完整的`SSH PRIVATE`金鑰值，包括頁首、頁尾和分行，以確保正確的加密／金鑰儲存。

### 外發時間不足

外框程式每天執行兩次，而且有多個程式（外框、發佈、推送至外部位置等） 必須在檔案推送至其最終目的地之前執行。 一個很好的經驗法則是，目標應至少在24小時內完全配置，您才能預期資料會推送至外部位置。

### 檔案分割大小過大

當將檔案外框至目的地時，您可以將較大的外框檔案分割為檔案區塊。 請確定個別檔案區塊不超過10 GB。 另請參閱[出站資料檔案名：語法與範例](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html)。


## 如何設定目的地以匯出傳出資料檔案中的Experience Cloud ID、客戶ID或Audience Manager ID {#set-up-destinations-export}

此頁顯示如何設定目標以導出在[!UICONTROL Outbound Data Files]中要輸入的ID類型的資料。

<!-- set-up-destinations-mcid-aamid.xml -->

目標可讓客戶透過任何數位通道啟動其資料。 例如，他們可將觀眾資料匯出至其他[!DNL Adobe Experience Cloud]解決方案（[!DNL Target]、[!DNL Campaign]等）。 或者，他們可以傳送資料至[!UICONTROL DSP]s、[!UICONTROL SSP]s或與Audience Manager整合的任何平台。 我們在[整合Wiki頁面](https://wiki.corp.adobe.com/display/MCPI)中保存與我們合作的合作夥伴清單。

>[!NOTE]
>
>如需有關在管理員UI中建立目標的詳細逐步說明，請參閱[建立或編輯公司目標](companies/admin-manage-company-destinations.md#create-edit-company-destinations)文章。

您的客戶想要匯出不同的ID類型，視目標而定。 下面的配置圖表顯示了應選擇哪些選項，以導出與不同ID類型相關的配置檔案資訊。 我們建議您也參考Audience Manager中的[ID索引](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)。 有三個重要的設定值需考慮： [!UICONTROL User ID Key]、[!UICONTROL Data Source Type]和[!UICONTROL Format]。 我們詳細說明下面的所有細節。

* [!UICONTROL User ID Key]。在[!UICONTROL Admin UI]中，轉至&#x200B;**[!UICONTROL Companies]**。 搜尋客戶的公司，然後按一下。 查找&#x200B;**[!UICONTROL Destinations]**&#x200B;頁籤，然後按&#x200B;**[!UICONTROL Add Destination]**。 在&#x200B;**[!UICONTROL Add Destination]**&#x200B;工作流中，選擇[!UICONTROL User ID Key]。 [!UICONTROL User ID Key]會篩選目標資料來源的傳入ID，並僅允許ID傳遞。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience Manager UI中建立目標時，請選取此選項。 首先，選擇[!UICONTROL Inbound]，然後選擇所需的ID類型。 選項包括：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此選項決定您要匯出的檔案格式。 在&#x200B;**[!UICONTROL Add Destination]**&#x200B;工作流的&#x200B;**[!UICONTROL Batch Data]**&#x200B;下，選擇格式。

要檢查格式，請轉至&#x200B;**[!UICONTROL Admin UI > Formats]**&#x200B;並查找[!UICONTROL Data Row]元素。 此元素包含檔案格式的巨集，&lt;MCID>如下例所示。

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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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

假設您使用Audience Manager和[!DNL Campaign]。 為了使客戶資料在[!DNL Campaign]中可操作，您要匯出[!UICONTROL Experience Cloud IDs]。 在這種情況下，應使用配置編號3。