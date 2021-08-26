---
description: 可協助您在Audience Manager中設定目的地，並避免常見問題的資訊。
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: 目的地設定疑難排解
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# 目的地設定疑難排解 {#destination-setup-troubleshooting}

可協助您在Audience Manager中設定目的地，並避免常見問題的資訊。

## 我設定了目的地，但沒看到任何檔案。 它們在哪裡？ {#destination-no-files}

<!-- c_dest_tshooting.xml -->

常見的目標配置問題包括以下問題：

### 目標配置錯誤

* **錯 [!UICONTROL UserID] 誤的索引鍵** : [!UICONTROL UserID] 索引鍵 [!UICONTROL MasterDPID] 是此目的地的，且是將會超出界限之ID值的基礎。即使可透過下拉式清單選取[!UICONTROL UserID]索引鍵，也不一定表示有對應至此值的ID/特徵/區段。 如果[!UICONTROL Outbound]進程（在建立目標後運行）找不到映射到此[!UICONTROL UserID]鍵的任何用戶，則不會有任何資料被外界限制。
* **未選取檔案資料來源：** 選擇除 [!UICONTROL S2S]外的任何目的地類型時，畫面底部會出現標示為的區 [!UICONTROL Configure Data Sources]段。首次出現此區段時，不會選取任何值。 如果您忘記按一下[!UICONTROL All First Party]核取方塊或從[!UICONTROL Available Data Sources]視窗中個別選取資料來源，則不會有任何資料被排除。

### 配置錯誤的格式

為外界資料選擇格式時，最好（如果可能）重新使用現有格式。 使用已驗證的格式，可確保成功產生傳出資料。 若要確切查看現有格式的格式，請按一下菜單欄中的[!UICONTROL Formats]選項，然後按名稱或ID號搜索格式。 格式中使用的格式錯誤或宏將提供格式錯誤的輸出，或將阻止完全輸出資訊。

有關設定格式和使用宏的詳細資訊，請參閱[檔案格式宏](formats/file-formats.md#)和[HTTP格式宏](formats/web-formats.md)。

### 伺服器配置錯誤

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 請勿為主機名輸入任何前置詞。 如果您有帳戶[!DNL ftp://hello.com]，只需在此欄位中輸入[!DNL hello.com]即可。
   * **[!UICONTROL Port/Type Combination]**
      * 對於[!DNL FTP]傳輸，首選傳輸類型為[!DNL SFTP]。
      * 選擇[!DNL SFTP]類型時，埠幾乎總是22。
      * 選擇[!DNL FTPs/TLS]類型時，埠幾乎總是21。
      * [!DNL FTPs/TLS]類型與常規[!DNL FTP]傳輸不同。 我們不支援常規（不安全）[!DNL FTP]傳輸。
   * **[!UICONTROL Remote Path]**
      * 選擇遠端子路徑時，應輸入該沒有前導斜線。
      * 如果傳輸的檔案應放置在[!DNL (root)/inbound]子資料夾中，只需為遠程路徑添加[!DNL inbound]，而不是[!DNL /inbound]。
      * 如果將檔案沿路徑發送多個目錄，請在每個目錄之間輸入斜線。 如果您獲得[!DNL /inbound/subdirectory1/subdirectory2]的位置，則應在此欄位中輸入[!DNL inbound/subdirectory1/subdirectory2]。
      * 如果檔案應放置在外部伺服器自動路由到的目錄中，則可將此空間留空。 請勿輸入句號(。 )、斜線(/)或其他任何項目。

* **[!DNL S3]**
   * [!DNL S3] 是慣用的傳輸通訊協定( [!DNL FTP] over或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 貯體名稱應列出，且不含斜線、前置詞、尾碼等。 如果給了地址[!DNL s3://your-bucket]，則只需將[!DNL your-bucket]添加到此欄位。
      * **[!UICONTROL Directory]**
         * 請將此欄位留空，除非您明確指定應將資料放入的子目錄。 如果給定了地址[!DNL s3://your-bucket/your-subdirectory]，請在[!UICONTROL Bucket]欄位中輸入[!DNL your-bucket]，並應將[!DNL your-subdirectory]添加到[!UICONTROL Directory]欄位中。 請勿新增先前的斜線。
         * 如果必須沿路徑傳送多個目錄，則只應使用斜線作為分隔符。 因此，[!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2]的位置將在[!UICONTROL Bucket]欄位中具有[!DNL your-bucket]，而在[!UICONTROL Directory]欄位中輸入了[!DNL your-subdirectory1/your-subdirectory2]。
      * **[!UICONTROL Access / Secret Keys]**
         * 當[!DNL TechOps]建立貯體並向顧問提供存取/機密金鑰時，這些憑證通常是要傳遞給用戶端的`READ-ONLY`憑證。 不應在[!UICONTROL Access / Secret Key]欄位中輸入這些憑據，因為這將導致傳輸失敗（因為這些憑據是只讀的，不可寫的）。 若[!DNL TechOps]建立貯體並提供憑證，顧問也應要求Adobe金鑰組（「不要指派給用戶端」），以允許將檔案寫入此貯體。 應將該索引鍵新增至這些欄位。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 請為[!DNL HTTP]條目輸入前置詞資訊。 如果您有帳戶[!DNL https://superduper.com]，請在此欄位中輸入[!DNL https://superduper.com]。
      * **[!UICONTROL URL Prefix]**
         * 新增[!DNL URL]首碼時，請將前一個斜線保留為關閉。 [!DNL https://hello.com/r/x/y/z]的地址應在[!UICONTROL Domain]欄位中輸入[!DNL https://hello.com]，在[!UICONTROL URL Prefix]欄位中輸入[!DNL r/x/y/z]。
         * 如果不需要[!UICONTROL URL Prefix]，請將此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 在此框中輸入完整的`SSH PRIVATE`鍵值，包括頁眉、頁腳和分行符，以確保準確的加密/密鑰儲存。

### 沒有足夠的時間生成出站

外界處理程式每天執行兩次，且執行多個處理（外界、發佈、推送至外部位置等） 必須先執行，檔案才會推送至其最終目的地。 理想的經驗法則是，目標應至少在24小時之後完全配置，您才能預期資料會推送至外部位置。

### 檔案拆分大小過大

將檔案外框到目標時，您可以將較大的外框檔案拆分為檔案塊。 請確定個別檔案區塊不超過10 GB。 另請參閱[傳出資料檔案名稱：語法和範例](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en)。


## 如何設定您的目的地，以匯出資料檔案中的Experience CloudID、客戶ID或Audience ManagerID {#set-up-destinations-export}

本頁面說明如何設定目的地，以匯出在[!UICONTROL Outbound Data Files]中輸入您所需ID類型的資料。

<!-- set-up-destinations-mcid-aamid.xml -->

目的地可讓客戶透過任何數量的數位通道啟用其資料。 例如，他們可以將受眾資料匯出至其他[!DNL Adobe Experience Cloud]解決方案（[!DNL Target]、[!DNL Campaign]等）。 或者，他們可以將資料傳送至[!UICONTROL DSP]s、[!UICONTROL SSP]s，或任何與Audience Manager整合的平台。 我們會在[整合Wiki頁面](https://wiki.corp.adobe.com/display/MCPI)上保存合作夥伴清單。

>[!NOTE]
>
>如需在管理員UI中建立目的地的詳細逐步說明，請參閱[建立或編輯公司目的地](companies/admin-manage-company-destinations.md#create-edit-company-destinations)文章。

您的客戶想要匯出不同的ID類型，視目的地而定。 下方的設定圖顯示您應選取的選項，以匯出與不同ID類型相關的設定檔資訊。 我們建議您也參考Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en)中的[ ID索引。 有三個重要設定需要考慮： [!UICONTROL User ID Key]、[!UICONTROL Data Source Type]和[!UICONTROL Format]。 我們詳細記錄了下面的所有內容。

* [!UICONTROL User ID Key]。在[!UICONTROL Admin UI]中，前往&#x200B;**[!UICONTROL Companies]**。 搜尋客戶的公司，然後按一下。 查找&#x200B;**[!UICONTROL Destinations]**&#x200B;頁簽，然後按&#x200B;**[!UICONTROL Add Destination]**。 在&#x200B;**[!UICONTROL Add Destination]**&#x200B;工作流程中，選取[!UICONTROL User ID Key]。 [!UICONTROL User ID Key]將篩選目標資料源中傳入的ID，並僅允許ID傳遞。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience ManagerUI中建立目的地時，請選取此選項。 首先，選擇[!UICONTROL Inbound]，然後選擇所需的ID類型。 選項為：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此選項決定要匯出的檔案格式。 在&#x200B;**[!UICONTROL Add Destination]**&#x200B;工作流程的&#x200B;**[!UICONTROL Batch Data]**&#x200B;下，選取格式。

要檢查格式，請轉至&#x200B;**[!UICONTROL Admin UI > Formats]**&#x200B;並查找[!UICONTROL Data Row]元素。 以下範例中，此元素包含檔案格式的巨集&lt;MCID>。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 配置編號 </th> 
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
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience CloudID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience CloudID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
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
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>客戶 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID（公司可存取的任何資料來源） </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用個案

假設您使用Audience Manager和[!DNL Campaign]。 為了讓客戶資料在[!DNL Campaign]中操作，您要匯出[!UICONTROL Experience Cloud IDs]。 在這種情況下，您應使用配置號3。
