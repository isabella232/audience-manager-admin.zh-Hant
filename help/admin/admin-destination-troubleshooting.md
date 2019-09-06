---
description: 這些資訊可協助您在Audience Manager中設定目的地，並避免常見問題。
seo-description: 這些資訊可協助您在Audience Manager中設定目的地，並避免常見問題。
seo-title: 目的地設定疑難排解
title: 目的地設定疑難排解
uuid: 04080fb9-6c7b-4de7-960e-54482be=
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# 目的地設定疑難排解 {#destination-setup-troubleshooting}

這些資訊可協助您在Audience Manager中設定目的地，並避免常見問題。

## 我設定了目的地，但看不到任何檔案。他們在哪裡？ {#destination-no-files}

<!-- c_dest_tshooting.xml -->

常見的目的地設定問題包括下列問題：

### 設定錯誤的目的地

* **[!UICONTROL UserID]錯誤索引鍵：**[!UICONTROL UserID] 索引鍵是此目的地的基礎 [!UICONTROL MasterDPID] ，且是ID值超出範圍的基礎。即使 [!UICONTROL UserID] 透過下拉式清單可選擇索引鍵，但並不一定表示有ID/特徵/區段對應至此值。[!UICONTROL Outbound] 如果程序(建立目的地後執行)找不到任何對應至此 [!UICONTROL UserID] 索引鍵的使用者，則沒有任何資料會超出界限。
* **未選取檔案資料來源：** 選擇以外的任何目的地類型 [!UICONTROL S2S]時，畫面底部會顯示一個區段 [!UICONTROL Configure Data Sources]。當第一個出現時，不會選取任何值。如果您忘記按一下 [!UICONTROL All First Party] 核取方塊或從 [!UICONTROL Available Data Sources] 視窗個別選取資料來源，則沒有任何資料會超出界限。

### 格式錯誤

為您的對外資料選擇格式時，可以盡可能地重復使用現有格式。使用已經證實可行的格式，可確保您的對外資料產生成功。若要確切檢視現有格式的格式，請按一下選單列 [!UICONTROL Formats] 中的選項，然後依名稱或ID編號搜尋格式。格式格式格式不正確或巨集會提供格式錯誤的輸出，或防止資訊完全輸出。

如需設定格式和使用巨集的詳細資訊，請參閱 [「檔案格式Macros](formats/file-formats.md#) 」和 [「HTTP格式巨集](formats/web-formats.md)」。

### 未設定的伺服器

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 請勿輸入主機名稱的任何字首。如果您已收到帳戶 [!DNL ftp://hello.com]，只需輸入 [!DNL hello.com] 此欄位即可。
   * **[!UICONTROL Port/Type Combination]**
      * [!DNL FTP] 對於轉讓，偏好的傳輸類型是 [!DNL SFTP]。
      * 在選取 [!DNL SFTP] 類型時，連接埠幾乎是22。
      * 在選取 [!DNL FTPs/TLS] 類型時，連接埠幾乎一律21。
      * [!DNL FTPs/TLS] 此類型與一般 [!DNL FTP] 傳輸不同。我們不支援定期(不安全) [!DNL FTP] 轉讓。
   * **[!UICONTROL Remote Path]**
      * 選擇遠端子路徑時，應輸入無前導斜線。
      * 如果您的傳輸檔案被放在 [!DNL (root)/inbound] 子檔案夾中，只需新增 [!DNL inbound] 遠端路徑，而 [!DNL /inbound]不要加入。
      * 如果您將多個目錄傳送到路徑，在每個目錄之間輸入斜線。如果您已獲得位置 [!DNL /inbound/subdirectory1/subdirectory2]，請在此欄位中輸入 [!DNL inbound/subdirectory1/subdirectory2] 。
      * 如果您的檔案應放置在外部伺服器自動路由到的目錄中，您可以將此空格留空。請勿輸入句點(.)、斜線(/)或其他任何項目。

* **[!DNL S3]**
   * [!DNL S3] 是偏好的傳輸通訊協定(over [!DNL FTP] 或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 儲存貯體名稱時，不會出現斜線、首碼、字尾等。如果您收到地址 [!DNL s3://your-bucket] ，只需新增 [!DNL your-bucket] 至此欄位。
      * **[!UICONTROL Directory]**
         * 除非您特別指定要放置資料的子目錄，否則將此欄位保留空白。如果您收到位址 [!DNL s3://your-bucket/your-subdirectory]，請輸入 [!DNL your-bucket][!UICONTROL Bucket] 欄位 [!DNL your-subdirectory] ，並加入 [!UICONTROL Directory] 欄位中。請勿新增先前的斜線。
         * 如果您必須沿著路徑移動多個目錄，則應使用斜線做為分隔符號。因此欄位中 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 的位置 [!DNL your-bucket][!UICONTROL Bucket] 會在欄位中輸入，並 [!DNL your-subdirectory1/your-subdirectory2] 進入 [!UICONTROL Directory] 欄位中。
      * **[!UICONTROL Access / Secret Keys]**
         * [!DNL TechOps] 建立儲存貯體並提供存取權/秘密金鑰給顧問時，這些憑證通常 `READ-ONLY` 是要交給用戶端的憑證。這些憑證不應輸入 [!UICONTROL Access / Secret Key] 到欄位中，因為這會導致傳輸失敗(因為這些認證是唯讀，無法寫入)。[!DNL TechOps] 在建立儲存貯體並提供憑證的情況下，顧問也應該要求Adobe金鑰配對-而不要授與用戶端-這會允許將檔案寫入此儲存貯體。該索引鍵應加入這些欄位中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 請輸入 [!DNL HTTP] 輸入的首碼資訊。如果您已收到帳戶 [!DNL https://superduper.com]，請在 [!DNL https://superduper.com] 此欄位中輸入。
      * **[!UICONTROL URL Prefix]**
         * 新增 [!DNL URL] 首碼時，請將先前的斜線離開。[!DNL https://hello.com/r/x/y/z] 應在欄位 [!DNL https://hello.com] 中輸入的位址 [!UICONTROL Domain] ， [!DNL r/x/y/z] 並在 [!UICONTROL URL Prefix] 欄位中輸入。
         * 如果不需要， [!UICONTROL URL Prefix] 請將此值保留空白。
      * **[!UICONTROL Authentication - SSH Key]**
         * 在此方塊中輸入完整 `SSH PRIVATE` 的關鍵值，包括頁首、頁尾和分行符號，以確保正確加密/金鑰儲存。

### 無足夠的對外產生時間

邊界程序每日執行兩次，且多個程序(邊界、發佈、推播至外部位置等)必須先執行，才能將檔案推送至其最終目的地。理想的提示法則是，目的地應至少設定24小時，才可預期資料將推送至外部位置。

### 檔案分割大小過大

將檔案外框至目的地時，您可以將較大的傳出檔案分割為檔案區塊。請確定個別檔案區塊不超過10GB。另請參閱 [對外資料檔案名稱：語法和範例](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html)。


## 如何設定您的目標在傳出資料檔案中匯出Experience Cloud ID、客戶ID或Audience Manager ID {#set-up-destinations-export}

此頁面顯示如何設定目的地，以隱藏您想要的 [!UICONTROL Outbound Data Files]ID類型的資料。

<!-- set-up-destinations-mcid-aamid.xml -->

目標可讓我們的客戶在任意數量的數位通道中啓動資料。例如，他們可以將觀眾資料匯出至其他 [!DNL Adobe Experience Cloud] 解決方案([!DNL Target]等 [!DNL Campaign])。或者，他們可以將資料傳送至 [!UICONTROL DSP]與Audience Manager整合的s、 [!UICONTROL SSP]s或任何平台。我們會在 [整合Wiki頁面](https://wiki.corp.adobe.com/display/MCPI)上，列出合作夥伴清單。

>[!NOTE]
>
>如需在管理UI中建立目的地的詳細逐步介紹，請參閱 [「建立或編輯公司目標](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 文章」。

您的客戶想要匯出不同的ID類型，視目的地而定。下表顯示您應該選取的選項，以匯出與不同ID類型相關的描述檔資訊。建議您也參考Audience Manager中的ID [索引](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)。有三項重要設定可考慮， [!UICONTROL User ID Key][!UICONTROL Data Source Type][!UICONTROL Format]包括和和。我們詳細說明它們。

* [!UICONTROL User ID Key]。[!UICONTROL Admin UI]**[!UICONTROL Companies]**&#x200B;請至。搜尋客戶的公司並按一下。尋找 **[!UICONTROL Destinations]** 標籤並按 **[!UICONTROL Add Destination]**&#x200B;一下。在 **[!UICONTROL Add Destination]** 工作流程中，選取 [!UICONTROL User ID Key]。它 [!UICONTROL User ID Key] 會從目標資料來源篩選傳入的ID，只允許傳送ID。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience Manager UI中建立目的地時，請選取此選項。首先，選取 [!UICONTROL Inbound]，然後選取您想要的ID類型。選項包括：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此選項會決定您要匯出的檔案格式。**[!UICONTROL Add Destination]** 在工作流程中 **[!UICONTROL Batch Data]**，選取格式。

若要檢查格式，請前往 **[!UICONTROL Admin UI > Formats]** 並尋找 [!UICONTROL Data Row] 元素。此元素包含檔案格式的巨集，如下範例所示。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 設定否。 </th> 
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
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p> </p> </td> 
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
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
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
   <td colname="col1"> <p>DPID(公司有權存取的任何資料來源) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
   <td colname="col4"> <p>客戶ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID(公司有權存取的任何資料來源) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID(公司有權存取的任何資料來源) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID(公司有權存取的任何資料來源) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID(公司有權存取的任何資料來源) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID(公司有權存取的任何資料來源) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用個案

假設您使用Audience Manager [!DNL Campaign]。為了讓客戶資料可運作，您 [!DNL Campaign]想要匯出 [!UICONTROL Experience Cloud IDs]。在此情況下，您應使用組態號碼3。