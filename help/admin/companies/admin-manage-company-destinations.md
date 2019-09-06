---
description: 建立、編輯和刪除Audience Manager目的地。
seo-description: 建立、編輯和刪除Audience Manager目的地。
seo-title: 管理公司目標
title: 管理公司目標
uuid: d9a6bfb1-7629-44e0-b7 d7-eg44 f65 ea2 b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 管理公司目標 {#manage-company-destinations}

建立、編輯和刪除Audience Manager目的地。

<!-- t_company_destinations.xml -->

如需詳細資訊，請參閱 [](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html)*觀眾管理員使用指南*&#x200B;中的目標。

## 建立或編輯公司目標 {#create-edit-company-destinations}

捲動各個區段，以取得如何建立新 [!DNL Audience Manager] 目的地或編輯現有目的地的逐步指示。

<!-- create-edit-company-destinations.xml -->

設定目的地之前，請先造訪 [Experience Cloud合作夥伴整合頁面](https://wiki.corp.adobe.com/x/mPIMPw) 。頁面包含您需要填寫每 [!DNL Audience Manager] 個合作夥伴整合所需的特定資訊。

如果您的客戶想要當做 [!DNL Adobe Media Optimizer] 目的地使用 [!DNL Audience Manager] ，您必須將此設定為 [!DNL Adobe Media Optimizer]一個。

## Navigate to the Destinations Tab {#navigate-destinations}

1. 按一下 **[!UICONTROL Companies]**，然後找出並按一下所需的公司以顯示其 [!UICONTROL Profile] 頁面。您可以使用 [!UICONTROL Search] 方塊底部或清單底部的分頁控制項來尋找所需的公司。您可以按一下所要的欄標題，以遞增或遞減順序排序每欄。
1. Click the **[!UICONTROL Destinations]** tab.
1. 若要建立新目的地，請按一下 **[!UICONTROL Add Destination]**。To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## 基本設定 {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]：** (必要)指定此目的地的名稱。
* **[!UICONTROL Description]：** 指定此目的地的描述性資訊。
* **[!UICONTROL Type]：** (必要)選擇所要的目的地類型：
   * **[!UICONTROL Bulk ID]**：同步不同平台之間的ID。
   * **[!UICONTROL Bulk Trait]**：大量傳送特徵資訊至不同平台。
   * **[!UICONTROL Bulk Segment]**：大量傳送區段資訊至不同平台。
   * **[!UICONTROL S2S]**：使用伺服器到伺服器目的地，將即時和批次資料傳送至不同平台。
* **[!UICONTROL Auto-Fill Destination Mapping]：** ( [!UICONTROL S2S] 僅限)選取一個選項：
   * **[!UICONTROL Segment ID]：** 如果您選取此設定，目標值對應會填入 [!DNL Audience Manager] 區段ID。
   * **[!UICONTROL Integration Code Value]：** 如果您選取此設定，目標值對應會填入 [!DNL Audience Manager] 區段整合代碼。
* **[!UICONTROL User ID Key]：** (必要)從下拉式清單中選擇所要的使用者ID金鑰。

此ID會用作主資料來源ID。這會判斷使用者ID在檔案中是否超出界限。

>[!NOTE]
>
>[!UICONTROL Bulk ID] 對於目的地類型，您無法使用 [!DNL Audience Manager][!UICONTROL User ID] 或 [!DNL Adobe Experience Cloud] ID。

如果您的資料來源ID( [!UICONTROL DPID])未顯示在下拉式清單中，則必須在資料 **[!UICONTROL Outbound]**[來源設定頁面](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)上選取資料來源層級的核取方塊。

* **[!UICONTROL Target Data Source]：** (必要)從下拉式清單中選擇所要的此目的地資料來源。此設定可讓您標記超出界限的資料，以便在用戶端的個別系統中擷取。
* **[!UICONTROL Foreign Account ID]：** 指定此目的地的國外帳戶ID。這是收件者系統中這個無界限資料的識別值。
* **[!UICONTROL Outbound Sample Rate Denominator]：** 當傳回的資料總金額未知時，請使用此設定來只傳回大量資料，而非完整金額。在此處調整數字以代表一小部分資料(例如，值'100'傳回1/100的一般資料量，'10'傳回1/10的普通資料量)。預設值為'1'，會傳回所有資料。

## 即時資料(適用於S2S目的地) {#realtime-s2s}

如果您要建立 [!UICONTROL S2S] 目的地，請填寫下列欄位：

**[!UICONTROL Servers]**：為此目的地選取所需 `HTTP` 的伺服器。
**[!UICONTROL Format]**：從下拉式清單中選擇所要的格式： [!UICONTROL HTTP only]。

>[!NOTE]
>
>您只需使用 [!DNL S2S] 螢幕關閉/開啓滑桿，即可啓用或停用任何或 [!UICONTROL Realtime][!UICONTROL Batch] 目的地。您無法停用這兩個選項。

## 批次資料 {#batch-data}

對於 [!UICONTROL Bulk ID]或 [!UICONTROL Bulk Trait][!UICONTROL Bulk Segment] 目的地，請填寫下列欄位：

* **[!UICONTROL Protocol]**：(必要)從下拉式清單中選取所需的通訊協定：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**：(必要)從下拉式清單中選擇所要的伺服器伺服器。
* **[!UICONTROL Format]**：(必要)從下拉式清單中選擇所要的格式格式： [!DNL HTTP] 或檔案類型，視您選擇的通訊協定而定。
* **[!UICONTROL Sync Type]**：(必要)選取此目的地所要的同步類型。這表示客戶希望包含在對外訂單中的使用者活動層級。選取 **[!UICONTROL Customer]** 客戶是否只想分析其屬性的區段資格。選擇 **[!UICONTROL Platform]** 是否要納入所有 [!DNL Audience Manager] 客戶之場外活動的區段資格。
* **[!UICONTROL Customer]**：檔案包含作用中使用者，只有在選定時段內，至少會對用戶端屬性(與用戶端 [!UICONTROL PID]相關)進行特徵實作。您的客戶應使用此選項將其 *即時* 細分資格外包至目的地。
* **[!UICONTROL Platform]**：檔案包含至少一個即時互動的作用中使用者，其ID同步或特徵實現在 [!DNL Audience Manager] 所有用戶端的屬性(與所有用戶端PILD關聯)在所選時段內的任何位置。您的客戶應使用此選項將其 ** 區段的總限定資格超出目的地。
* **[!UICONTROL Lifetime]**：檔案包含自建立目的地後所有 [!DNL Audience Manager] 用戶端屬性中所有用戶端屬性的任何位置。
* **[!UICONTROL Sync Type Lookback Period]**：如果您選取 [!UICONTROL Customer] 或 [!UICONTROL Platform]選擇時段。檔案包含所選時段內的作用中使用者。
接著，選取訂單類型。這表示每個對外整合的頻率和範圍。在遞增和完整訂購之間進行選擇。
* **[!UICONTROL Incremental Scheduled Run]**：每次執行 [!DNL Audience Manager] 時，只會傳出自上一張傳出訂單後的新使用者資格。選擇您要 [!DNL Audience Manager] 執行增量同步程序的時段。例如，您可以每24小時、每七天、每30天或從未選取一次。

>[!NOTE] {importance=「high」}
>
>第一個遞增的訂單等同於完整訂購，因為先前沒有任何使用者傳送到目的地。

* **[!UICONTROL Full Sync Scheduled Run]**：每次執行後， [!DNL Audience Manager] 在首次設定目的地後，將會傳出所有作用中使用者。選取想要使用的計劃， [!DNL Audience Manager] 以執行完全同步程序。例如，您可以每24小時、每七天、每30天或從未選取一次。

>[!NOTE] {importance=「high」}
>
>我們建議使用漸進式同步比完整同步更頻繁。漸進式同步只傳送包含新特性實作或ID同步的檔案。完整語法會傳送所有檔案，不論它們是否包含新實作或ID同步。只有當客戶需要完整的副本時，才會使用 [!UICONTROL Full Sync Scheduled Run] 組態來減少傳出資料量。

## 設定資料來源 {#configure-data-sources}

對於 [!UICONTROL Bulk ID]或 [!UICONTROL Bulk Trait][!UICONTROL Bulk Segment] 目的地，請填寫下方的欄位。這些設定可讓您根據與資料來源關聯的類型傳送所有資料(特徵、區段或ID)。

* **[!UICONTROL All Unrestricted First Party Data]**：選擇使用所有第一方資料來源。如果您選取此選項， [!UICONTROL Available Data Sources] 則會停用選項。
* **[!UICONTROL Available Data Sources]**：使用箭頭來移動 **[!UICONTROL Available Data Sources]****[!UICONTROL In File Data Sources]** 和方塊之間的資料來源。

## 儲存並完成 {#save-and-finalize}

**[!UICONTROL Save]** 在填寫所有必要欄位後，按鈕會啓動。按一下 **[!UICONTROL Save]** 以完成建立目的地程序。

## 刪除公司目標 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

若要刪除目的地：

1. 按一下 **[!UICONTROL Companies]**，找到並按一下所需的公司，然後按一下 **[!UICONTROL Destinations]** 標籤。
1. 按一下 ![](assets/icon_delete.png) 所要目的地 **[!UICONTROL Actions]** 的欄。
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>如果目的地已對應至該目的地，則無法刪除該目的地。