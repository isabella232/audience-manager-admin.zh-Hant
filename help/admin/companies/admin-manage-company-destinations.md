---
description: 建立、編輯和刪除Audience Manager目的地。
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: 管理公司目的地
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# 管理公司目的地 {#manage-company-destinations}

建立、編輯和刪除Audience Manager目的地。

<!-- t_company_destinations.xml -->

如需詳細資訊，請參閱&#x200B;*Audience Manager使用手冊*&#x200B;中的[目標](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html)。

## 建立或編輯公司目的地 {#create-edit-company-destinations}

捲動各區段，以取得如何建立新[!DNL Audience Manager]目的地或編輯現有目的地的逐步指示。

<!-- create-edit-company-destinations.xml -->

在設定目的地之前，請造訪[Experience Cloud合作夥伴整合頁面](https://wiki.corp.adobe.com/x/mPIMPw)。 該頁面包含您為每個[!DNL Audience Manager]合作夥伴整合所需填入的特定資訊。

如果您的客戶希望使用[!DNL Adobe Media Optimizer]作為[!DNL Audience Manager]中的目標，則需要在[!DNL Adobe Media Optimizer]中設定此設定。

## 導覽至「目的地」標籤 {#navigate-destinations}

1. 按一下「**[!UICONTROL Companies]**」，然後找出並按一下所需的公司，以顯示其「[!UICONTROL Profile]」頁面。 您可以使用[!UICONTROL Search]方塊或清單底部的分頁控制項來尋找所需的公司。 您可以按一下所需欄的標題，以遞增或遞減順序排序每個欄。
1. 按一下&#x200B;**[!UICONTROL Destinations]**&#x200B;標籤。
1. 要建立新目標，請按一下&#x200B;**[!UICONTROL Add Destination]**。 要編輯現有目標，請在&#x200B;**[!UICONTROL Name]**&#x200B;列中按一下目標的名稱。

## 基本設定 {#basic-settings}

填寫&#x200B;**[!UICONTROL Basic Settings]**&#x200B;窗口中的欄位。

* **[!UICONTROL Name]:** （必要）指定此目的地的名稱。
* **[!UICONTROL Description]:** 指定此目的地的說明性資訊。
* **[!UICONTROL Type]:** （必要）選取所需的目的地類型：
   * **[!UICONTROL Bulk ID]**:在不同平台之間同步ID。
   * **[!UICONTROL Bulk Trait]**:大量傳送特徵資訊至不同平台。
   * **[!UICONTROL Bulk Segment]**:大量傳送區段資訊至不同平台。
   * **[!UICONTROL S2S]**:使用伺服器對伺服器目的地將即時和批次資料傳送至不同平台。
* **[!UICONTROL Auto-Fill Destination Mapping]:** (僅 [!UICONTROL S2S] 限)選取選項：
   * **[!UICONTROL Segment ID]:** 如果您選取此設定，則目標值對應會填入 [!DNL Audience Manager] 區段ID。
   * **[!UICONTROL Integration Code Value]:** 如果您選取此設定，目標值對應會填入區段 [!DNL Audience Manager] 整合代碼。
* **[!UICONTROL User ID Key]:** （必要）從下拉式清單中選取此目的地的所需使用者ID金鑰。

此ID會作為主資料來源ID。 這會決定要在檔案中對外界定的使用者ID。

>[!NOTE]
>
>對於[!UICONTROL Bulk ID]目標類型，您不能使用[!DNL Audience Manager] [!UICONTROL User ID]或[!DNL Adobe Experience Cloud] ID。

如果您的資料來源ID([!UICONTROL DPID])未顯示在下拉式清單中，您必須在[資料來源設定頁面](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html)上的資料來源層級選取&#x200B;**[!UICONTROL Outbound]**&#x200B;核取方塊。

* **[!UICONTROL Target Data Source]:** （必要）從下拉式清單中選取此目的地的所需資料來源。此設定可標籤外界資料，以便將內容擷取至用戶端的個別系統。
* **[!UICONTROL Foreign Account ID]:** 指定此目的地的外來帳戶ID。這是收件者系統中此外界資料的識別值。
* **[!UICONTROL Outbound Sample Rate Denominator]:** 當傳回的資料總量未知時，請使用此設定僅傳回資料的範例量，而非完整量。在此調整數字以表示資料的一小部分(例如，值「100」會傳回1/100正常資料量，值「10」會傳回1/10正常資料量)。 預設為&#39;1&#39;，會傳回所有資料。

## 即時資料（適用於S2S目的地） {#realtime-s2s}

如果您要建立[!UICONTROL S2S]目的地，請填入下列欄位：

**[!UICONTROL Servers]**:為此目標 `HTTP` 選擇所需的伺服器。**[!UICONTROL Format]**:從下拉式清單中選取此目的地的所需格式： [!UICONTROL HTTP only].

>[!NOTE]
>
>僅對於[!DNL S2S]，可以使用螢幕上的「關閉」/「開啟」滑塊啟用或禁用[!UICONTROL Realtime]或[!UICONTROL Batch]目標。 不能同時禁用兩個選項。

## 批次資料 {#batch-data}

若為[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目的地，請填入下列欄位：

* **[!UICONTROL Protocol]**:（必要）從下拉式清單中選取此目的地的所需通訊協定：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:（必要）從下拉式清單中選取此目的地所需的伺服器。
* **[!UICONTROL Format]**:（必要）從下拉式清單中選取此目的地的所需格式： [!DNL HTTP] 或檔案類型，具體取決於您選擇的上述協定。
* **[!UICONTROL Sync Type]**:（必要）為此目標選擇所需的同步類型。這表示用戶端要納入對外訂單的使用者活動層級。 如果客戶只想從其屬性中分析區段資格，請選擇&#x200B;**[!UICONTROL Customer]**。 如果想包含所有[!DNL Audience Manager]客戶之離站活動的區段資格，請選取&#x200B;**[!UICONTROL Platform]**。
* **[!UICONTROL Customer]**:檔案包含的活動用戶在所選時段內，至少只有1個特徵實現(與客戶端的 [!UICONTROL PID]屬性關聯)。您的客戶應使用此選項將其&#x200B;*即時*&#x200B;區段資格傳出至目的地。
* **[!UICONTROL Platform]**:檔案包含在選定時段內，在所有客戶端屬性（與所有客戶端PID關聯）的任 [!DNL Audience Manager] 意位置至少具有1個即時交互的活動用戶，無論是ID同步還是特徵實現。您的客戶應使用此選項將其&#x200B;*total*&#x200B;區段資格傳出至目的地。
* **[!UICONTROL Lifetime]**:檔案包含自目標建立以來，在所有 [!DNL Audience Manager] 客戶端屬性上都可看到的活動用戶。
* **[!UICONTROL Sync Type Lookback Period]**:如果您選 [!UICONTROL Customer] 取或 [!UICONTROL Platform]，請選取時段。檔案包含所選時段的活動用戶。
接下來，選擇訂單類型。 這表示每個與合作夥伴的對外整合的頻率和範圍。 在增量訂單和完整訂單之間選擇。
* **[!UICONTROL Incremental Scheduled Run]**:每次執行時， [!DNL Audience Manager] 只會傳出自上次傳出訂單以來合格的淨新使用者。選擇希望[!DNL Audience Manager]執行增量同步進程的所需時段。 例如，您可以選取每24小時、每7天、每30天或從不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一個增量訂單等同於完整訂單，因為之前從未將任何使用者傳送至目的地。

* **[!UICONTROL Full Sync Scheduled Run]**:每次執行時， [!DNL Audience Manager] 都會傳出自目標首次設定以來的所有作用中使用者。選擇希望[!DNL Audience Manager]用於執行完全同步進程的計畫。 例如，您可以選取每24小時、每7天、每30天或從不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>建議使用增量同步的頻率比完全同步的頻率要高。 增量同步只會傳送包含新特徵實現或ID同步的檔案。 完全同步會傳送所有檔案，不論其是否包含新實現或ID同步。 當客戶端需要其所有用戶的完整副本時，僅使用[!UICONTROL Full Sync Scheduled Run]配置來減少出站資料卷。

## 設定資料來源 {#configure-data-sources}

若為[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目的地，請填入下列欄位。 這些設定可讓您根據選取的類型傳送與資料來源相關聯的所有資料（特徵、區段或ID）。

* **[!UICONTROL All Unrestricted First Party Data]**:選取「 」以使用所有第一方資料來源。如果選擇此選項，將禁用[!UICONTROL Available Data Sources]選項。
* **[!UICONTROL Available Data Sources]**:使用箭頭在和方塊之間移動資 **[!UICONTROL Available Data Sources]** 料 **[!UICONTROL In File Data Sources]** 來源。

## 儲存並完成 {#save-and-finalize}

填入所有必填欄位後，會啟動&#x200B;**[!UICONTROL Save]**&#x200B;按鈕。 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以完成建立目標進程。

## 刪除公司目的地 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

刪除目標：

1. 按一下「**[!UICONTROL Companies]**」，找出並按一下所需的公司，然後按一下「**[!UICONTROL Destinations]**」標籤。
1. 按一下所需目的地&#x200B;**[!UICONTROL Actions]**&#x200B;欄中的![](assets/icon_delete.png) 。
1. 按一下&#x200B;**[!UICONTROL OK]**&#x200B;以確認刪除。

>[!NOTE]
>
>如果目的地已對應區段，則無法刪除該目的地。
