---
description: 建立、編輯和刪除Audience Manager目標。
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

建立、編輯和刪除Audience Manager目標。

<!-- t_company_destinations.xml -->

有關詳細資訊，請參見 [目標](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) 的 *Audience Manager使用手冊*。

## 建立或編輯公司目的地 {#create-edit-company-destinations}

滾動各節，瞭解有關如何建立新文檔的逐步說明 [!DNL Audience Manager] 目標或編輯現有目標。

<!-- create-edit-company-destinations.xml -->

訪問 [Experience Cloud合作夥伴整合頁](https://wiki.corp.adobe.com/x/mPIMPw) 設定目標之前。 該頁面包含您需要為每個頁面填寫的特定資訊 [!DNL Audience Manager] 合作夥伴整合。

如果你的委託人想 [!DNL Adobe Media Optimizer] 作為 [!DNL Audience Manager] 你需要在 [!DNL Adobe Media Optimizer]。

## 定位至目標標籤 {#navigate-destinations}

1. 按一下 **[!UICONTROL Companies]**，然後找到並按一下所需的公司以顯示其 [!UICONTROL Profile] 的子菜單。 您可以使用 [!UICONTROL Search] 或清單底部的分頁控制項，以查找所需的公司。 通過按一下所需列的標題，可以按升序或降序對每列進行排序。
1. 按一下 **[!UICONTROL Destinations]** 頁籤。
1. 要建立新目標，請按一下 **[!UICONTROL Add Destination]**。 要編輯現有目標，請按一下 **[!UICONTROL Name]** 的雙曲餘切值。

## 基本設定 {#basic-settings}

填寫 **[!UICONTROL Basic Settings]** 的子菜單。

* **[!UICONTROL Name]:** （必需）指定此目標的名稱。
* **[!UICONTROL Description]:** 指定有關此目標的描述性資訊。
* **[!UICONTROL Type]:** （必需）選擇所需的目標類型：
   * **[!UICONTROL Bulk ID]**:在不同平台之間同步ID。
   * **[!UICONTROL Bulk Trait]**:將特性資訊批量發送到不同的平台。
   * **[!UICONTROL Bulk Segment]**:將段資訊批量發送到不同的平台。
   * **[!UICONTROL S2S]**:使用伺服器到伺服器目標向不同平台發送即時和批處理資料。
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] 僅)選擇選項：
   * **[!UICONTROL Segment ID]:** 如果選擇此設定，則目標值映射將填充 [!DNL Audience Manager] 段ID。
   * **[!UICONTROL Integration Code Value]:** 如果選擇此設定，則目標值映射將填充 [!DNL Audience Manager] 段整合代碼。
* **[!UICONTROL User ID Key]:** （必需）從下拉清單中選擇此目標所需的用戶ID鍵。

此ID用作主資料源ID。 這確定檔案中要超出的用戶ID。

>[!NOTE]
>
>對於 [!UICONTROL Bulk ID] 目標類型，不能使用 [!DNL Audience Manager] [!UICONTROL User ID] 或 [!DNL Adobe Experience Cloud] ID。

如果資料源ID( [!UICONTROL DPID])不顯示在下拉清單中，必須選擇 **[!UICONTROL Outbound]** 複選框。 [「資料源設定」頁](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html)。

* **[!UICONTROL Target Data Source]:** （必需）從下拉清單中選擇此目標的所需資料源。 此設定允許對外界資料進行標籤，這允許將資料攝取到客戶端的獨立系統中。
* **[!UICONTROL Foreign Account ID]:** 指定此目標的外來帳戶ID。 這是收件人系統中此外界資料的標識值。
* **[!UICONTROL Outbound Sample Rate Denominator]:** 當返回的資料總量未知時，使用此設定只返回資料的樣本量，而不是全部資料量。 在此調整數字以表示資料的一小部分（例如，值「100」返回常規資料量的1/100，值「10」返回常規資料量的1/10）。 預設值為「1」，返回所有資料。

## 即時資料（用於S2S目標） {#realtime-s2s}

如果要建立 [!UICONTROL S2S] 目標，填寫以下欄位：

**[!UICONTROL Servers]**:選擇所需 `HTTP` 此目標的伺服器。
**[!UICONTROL Format]**:從下拉清單中選擇此目標的所需格式： [!UICONTROL HTTP only]。

>[!NOTE]
>
>對於 [!DNL S2S] 只能啟用或禁用 [!UICONTROL Realtime] 或 [!UICONTROL Batch] 使用螢幕「關閉/開啟」滑塊的目標。 不能同時禁用這兩個選項。

## 批處理資料 {#batch-data}

對於 [!UICONTROL Bulk ID]。 [!UICONTROL Bulk Trait] 或 [!UICONTROL Bulk Segment] 目標，填寫以下欄位：

* **[!UICONTROL Protocol]**:（必需）從下拉清單中選擇此目標的所需協定：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:（必需）從下拉清單中選擇此目標所需的伺服器。
* **[!UICONTROL Format]**:（必需）從下拉清單中選擇此目標的所需格式： [!DNL HTTP] 或檔案類型，具體取決於您選擇的上述協定。
* **[!UICONTROL Sync Type]**:（必需）為此目標選擇所需的同步類型。 這表示客戶端希望包括在出站訂單中的用戶活動級別。 選擇 **[!UICONTROL Customer]** 客戶僅有興趣從其物業分析分部資格。 選擇 **[!UICONTROL Platform]** 如果他們希望包括所有非現場活動的段資格 [!DNL Audience Manager] 客戶。
* **[!UICONTROL Customer]**:檔案包含至少在客戶端屬性上具有1個特性的活動用戶（與客戶端的屬性關聯） [!UICONTROL PID])。 您的客戶應使用此選項將其 *即時* 將限定段限定到目標。
* **[!UICONTROL Platform]**:檔案包含至少具有1個即時交互的活動用戶，無論是ID同步還是特性實現，都可在所有位置進行 [!DNL Audience Manager] 所選時間段的客戶端屬性（與所有客戶端PID關聯）。 您的客戶應使用此選項將其 *合計* 將限定段限定到目標。
* **[!UICONTROL Lifetime]**:檔案包含所有位置都可見的活動用戶 [!DNL Audience Manager] 自目標建立以來的客戶端屬性。
* **[!UICONTROL Sync Type Lookback Period]**:如果選擇 [!UICONTROL Customer] 或 [!UICONTROL Platform]，選擇一個時段。 檔案包含所選時段的活動用戶。
接下來，選擇訂單類型。 這表示每個與合作夥伴的出站整合的頻率和範圍。 在增量訂單和完整訂單之間進行選擇。
* **[!UICONTROL Incremental Scheduled Run]**:每次跑， [!DNL Audience Manager] 將僅出站自上一個出站訂單以來合格的淨新用戶。 選擇所需的時段 [!DNL Audience Manager] 執行增量同步進程。 例如，您可以每24小時、每7天、每30天或從不選擇一次。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一個增量訂單相當於一個完整訂單，因為以前從未向目標發送過任何用戶。

* **[!UICONTROL Full Sync Scheduled Run]**:每次跑， [!DNL Audience Manager] 將出站自首次設定目標以來的所有活動用戶。 選擇所需的計畫 [!DNL Audience Manager] 用於執行完全同步進程。 例如，您可以每24小時、每7天、每30天或從不選擇一次。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>我們建議使用增量同步比使用完整同步更頻繁。 增量同步僅發送包含新特性實現或ID同步的檔案。 完整同步發送所有檔案，無論它們是否包含新實現或ID同步。 僅使用 [!UICONTROL Full Sync Scheduled Run] 配置時需要所有用戶的完整副本，以減少出站資料卷。

## 配置資料源 {#configure-data-sources}

對於 [!UICONTROL Bulk ID]。 [!UICONTROL Bulk Trait] 或 [!UICONTROL Bulk Segment] 目標，填寫下面的欄位。 這些設定允許您根據選定的類型發送與資料源關聯的所有資料（特徵、段或ID）。

* **[!UICONTROL All Unrestricted First Party Data]**:選擇以使用所有第一方資料源。 如果選擇此選項， [!UICONTROL Available Data Sources] 選項。
* **[!UICONTROL Available Data Sources]**:使用箭頭在 **[!UICONTROL Available Data Sources]** 和 **[!UICONTROL In File Data Sources]** 框。

## 保存並完成 {#save-and-finalize}

的 **[!UICONTROL Save]** 按鈕。 按一下 **[!UICONTROL Save]** 完成建立目標進程。

## 刪除公司目標 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

要刪除目標：

1. 按一下 **[!UICONTROL Companies]**，找到並按一下所需的公司，然後按一下 **[!UICONTROL Destinations]** 頁籤。
1. 按一下  ![](assets/icon_delete.png) 的 **[!UICONTROL Actions]** 目標的列。
1. 按一下 **[!UICONTROL OK]** 確認刪除。

>[!NOTE]
>
>如果目標具有映射到它的段，則不能刪除它。
