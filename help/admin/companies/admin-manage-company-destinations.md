---
description: 建立、編輯和刪除Audience Manager目標。
seo-description: 建立、編輯和刪除Audience Manager目標。
seo-title: 管理公司目的地
title: 管理公司目的地
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: f247457004a624297ddc8847dd256dbb7d8da418
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 1%

---


# 管理公司目的地{#manage-company-destinations}

建立、編輯和刪除Audience Manager目標。

<!-- t_company_destinations.xml -->

如需詳細資訊，請參閱&#x200B;*Audience Manager使用指南*&#x200B;中的[目標](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html)。

## 建立或編輯公司目的地{#create-edit-company-destinations}

捲動各節，以瞭解如何建立新[!DNL Audience Manager]目標或編輯現有目標的逐步指示。

<!-- create-edit-company-destinations.xml -->

在設定目標之前，請造訪[Experience Cloud合作夥伴整合頁面](https://wiki.corp.adobe.com/x/mPIMPw)。 該頁包含您需要填寫的特定資訊，以用於每個[!DNL Audience Manager]合作夥伴整合。

如果您的客戶想要在[!DNL Audience Manager]中使用[!DNL Adobe Media Optimizer]作為目標，則需要在[!DNL Adobe Media Optimizer]中設定此設定。

## 導覽至「目標」標籤{#navigate-destinations}

1. 按一下&#x200B;**[!UICONTROL Companies]**，然後找出並按一下所要的公司，以顯示其[!UICONTROL Profile]頁面。 您可以使用[!UICONTROL Search]方塊或清單底部的編頁控制項來尋找所需的公司。 您可以按一下所需欄的標題，以遞增或遞減順序來排序每個欄。
1. 按一下&#x200B;**[!UICONTROL Destinations]**&#x200B;頁籤。
1. 要建立新目標，請按一下&#x200B;**[!UICONTROL Add Destination]**。 要編輯現有目標，請在&#x200B;**[!UICONTROL Name]**&#x200B;列中按一下目標名稱。

## 基本設定{#basic-settings}

填寫&#x200B;**[!UICONTROL Basic Settings]**&#x200B;視窗中的欄位。

* **[!UICONTROL Name]:** （必要）指定此目標的名稱。
* **[!UICONTROL Description]：指** 定有關此目標的說明性資訊。
* **[!UICONTROL Type]:** （必要）選擇所需的目標類型：
   * **[!UICONTROL Bulk ID]**:在不同平台之間同步ID。
   * **[!UICONTROL Bulk Trait]**:大量傳送特徵資訊至不同平台。
   * **[!UICONTROL Bulk Segment]**:大量傳送區段資訊至不同的平台。
   * **[!UICONTROL S2S]**:使用伺服器對伺服器目的地，將即時和批次資料傳送至不同的平台。
* **[!UICONTROL Auto-Fill Destination Mapping]:** (僅 [!UICONTROL S2S] 限)選擇一個選項：
   * **[!UICONTROL Segment ID]:** 如果您選取此設定，目標值對應會填入區 [!DNL Audience Manager] 段ID。
   * **[!UICONTROL Integration Code Value]：如** 果您選取此設定，目標值對應會填入區段 [!DNL Audience Manager] 整合代碼。
* **[!UICONTROL User ID Key]:** （必要）從下拉式清單中選取此目標所要的使用者ID金鑰。

此ID用作主資料來源ID。 這會決定在檔案中的使用者ID被排除出界。

>[!NOTE]
>
>對於[!UICONTROL Bulk ID]目標類型，不能使用[!DNL Audience Manager] [!UICONTROL User ID]或[!DNL Adobe Experience Cloud] ID。

如果您的資料來源ID([!UICONTROL DPID])未顯示在下拉式清單中，您必須在[「資料來源設定」頁面](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)的資料來源層級選取&#x200B;**[!UICONTROL Outbound]**&#x200B;核取方塊。

* **[!UICONTROL Target Data Source]:** （必要）從下拉式清單中選取此目的地的所需資料來源。此設定允許標籤外界資料，這允許將資料提取到客戶端的獨立系統中。
* **[!UICONTROL Foreign Account ID]：指** 定此目標的外來帳戶ID。這是收件者系統中此外界資料的識別值。
* **[!UICONTROL Outbound Sample Rate Denominator]:** 當傳回的資料總量未知時，請使用此設定僅傳回資料的樣本量，而非全部量。在此處調整數字以代表資料的一部分（例如，&#39;100&#39;的值會傳回一般資料量的1/100,&#39;10&#39;的值會傳回一般資料量的1/10）。 預設值為&#39;1&#39;，會傳回所有資料。

## 即時資料（用於S2S目標）{#realtime-s2s}

如果您要建立[!UICONTROL S2S]目標，請填寫下列欄位：

**[!UICONTROL Servers]**:為此目標選 `HTTP` 擇所需的伺服器。**[!UICONTROL Format]**:從下拉式清單中選取此目標的所需格式： [!UICONTROL HTTP only].

>[!NOTE]
>
>僅適用於[!DNL S2S]，您可以使用螢幕上的「關閉／開啟」滑桿啟用或停用[!UICONTROL Realtime]或[!UICONTROL Batch]目標。 您無法同時停用這兩個選項。

## 批資料{#batch-data}

對於[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目標，請填寫以下欄位：

* **[!UICONTROL Protocol]**:（必要）從下拉式清單中選取此目的地的所需通訊協定：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:（必要）從下拉式清單中選取此目的地的伺服器。
* **[!UICONTROL Format]**:（必要）從下拉式清單中選取此目標的所需格式： [!DNL HTTP] 或檔案類型，視您上述選擇的通訊協定而定。
* **[!UICONTROL Sync Type]**:（必要）為此目標選擇所需的同步類型。這表示客戶希望包括在出站訂單中的用戶活動級別。 如果客戶只想從其屬性分析區段資格，請選取&#x200B;**[!UICONTROL Customer]**。 如果&#x200B;**[!UICONTROL Platform]**&#x200B;要納入所有[!DNL Audience Manager]客戶非現場活動的區段資格，請選擇&lt;a0/>。
* **[!UICONTROL Customer]**:檔案包含在選取時段內，至少只有在用戶端屬性（與用戶端相關聯）上具有1個特徵 [!UICONTROL PID]的作用中使用者。您的客戶應使用此選項將其&#x200B;*即時*&#x200B;區段資格傳出至目標。
* **[!UICONTROL Platform]**:檔案包含在選取時段內，在所有用戶端屬性（與所有用戶端PID相關聯）的任何位置，至少有1個即時互動（無論是ID同步或特徵實現）的作用中使用者。 [!DNL Audience Manager] 您的客戶應使用此選項將其&#x200B;*total*&#x200B;區段資格傳出至目標。
* **[!UICONTROL Lifetime]**:自目標建立以來，檔案包含在所有客 [!DNL Audience Manager] 戶端屬性中任何位置都可以看到的活動用戶。
* **[!UICONTROL Sync Type Lookback Period]**:如果您選 [!UICONTROL Customer] 擇 [!UICONTROL Platform]或，請選擇時段。檔案包含所選時段內的作用中使用者。
接著，選取訂單類型。 這表示每個與合作夥伴的對外整合的頻率和範圍。 在增量訂單和完整訂單之間進行選擇。
* **[!UICONTROL Incremental Scheduled Run]**:每次執行時， [!DNL Audience Manager] 僅會將自上一份出站訂單以來符合條件的淨新用戶出站。選擇希望[!DNL Audience Manager]執行增量同步進程的所需時段。 例如，您可以每24小時、每7天、每30天或從不選擇一次。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一個遞增的訂單等同於完整訂單，因為之前從未有任何使用者被傳送到目的地。

* **[!UICONTROL Full Sync Scheduled Run]**:每次執行時， [!DNL Audience Manager] 都會將目標首次設定後的所有作用中使用者對外傳出。選擇希望[!DNL Audience Manager]用於執行完全同步進程的所需計畫。 例如，您可以每24小時、每7天、每30天或從不選擇一次。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>我們建議使用增量同步比使用完整同步更頻繁。 增量同步只傳送包含新特徵實現或ID同步的檔案。 完整同步會傳送所有檔案，不論檔案是否包含新的實現或ID同步。 僅當客戶端需要所有用戶的完整副本時，才使用[!UICONTROL Full Sync Scheduled Run]配置來減少出站資料卷。

## 設定資料來源{#configure-data-sources}

對於[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目標，請填寫以下欄位。 這些設定可讓您根據選取的類型傳送與資料來源相關的所有資料（特徵、區段或ID）。

* **[!UICONTROL All Unrestricted First Party Data]**:選擇以使用所有第一方資料來源。如果選擇此選項，則[!UICONTROL Available Data Sources]選項將被禁用。
* **[!UICONTROL Available Data Sources]**:使用箭頭在和方塊之間移動 **[!UICONTROL Available Data Sources]** 資 **[!UICONTROL In File Data Sources]** 料來源。

## 保存並完成{#save-and-finalize}

**[!UICONTROL Save]**&#x200B;按鈕會在填入所有必要欄位後啟動。 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以最終確定建立目標進程。

## 刪除公司目標{#delete-company-destinations}

<!-- delete-company-destinations.xml -->

要刪除目標：

1. 按一下&#x200B;**[!UICONTROL Companies]**，找出並按一下所要的公司，然後按一下&#x200B;**[!UICONTROL Destinations]**&#x200B;標籤。
1. 按一下所要目的地之&#x200B;**[!UICONTROL Actions]**&#x200B;欄中的![](assets/icon_delete.png)。
1. 按一下&#x200B;**[!UICONTROL OK]**&#x200B;確認刪除。

>[!NOTE]
>
>如果目標的區段已映射至目標，則無法刪除目標。