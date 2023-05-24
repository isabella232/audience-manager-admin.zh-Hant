---
description: 使用Audience Manager管理工具中的「公司」頁面來建立新公司。
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: 建立公司設定檔
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 4%

---

# 建立公司設定檔 {#create-a-company-profile}

使用 [!UICONTROL Companies] 頁面(在Audience Manager管理工具中)來建立新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必須擁有 **[!UICONTROL DEXADMIN]** 角色以建立新公司。

1. 按一下 **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. 填寫欄位: 

   * **[!UICONTROL Name]**：（必要）指定公司名稱。
   * **[!UICONTROL Description]**：（必要）提供公司的描述性資訊，例如產業或其全名。
   * **[!UICONTROL Subdomain]**：（必要）指定公司的子網域。 您輸入的文字會顯示為事件呼叫的子網域。 無法變更此設定。 它必須是字串 [!DNL URL] — 有效字元。

      例如，如果貴公司名為 [!DNL AcmeCorp]，子網域會是 [!DNL acmecorp].

      Audience Manager會將子網域用於 [!UICONTROL Data Collection Server] (DCS)。 在上一個範例中，如果您的公司已滿 [!DNL URL] 在 [!UICONTROL DCS] 會是 [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**：指定公司需要的階段：
      * **[!UICONTROL Active]**：指定該公司將成為作用中Audience Manager使用者端。 一個 [!UICONTROL Active] 帳戶是指付費客戶，不僅是為了諮詢，也是為了提供Audience ManagerSKU。
      * **[!UICONTROL Demo]**：指定公司僅供示範用途。 系統會自動偽造報表資料。
      * **[!UICONTROL Prospect]**：指定該公司是潛在的Audience Manager客戶，例如可免費使用的公司 [!DNL POC] 或銷售示範的帳戶設定。
      * **[!UICONTROL Test]**：指定公司僅供內部測試之用。
   * **[!UICONTROL Account Types]**：指定此公司的完整帳戶型別集。 沒有帳戶型別與任何其他型別互斥。
      * **[!UICONTROL Full AAM]**：指定公司將擁有完整的Adobe Audience Manager帳戶，且使用者將擁有登入存取權。
      * **[!UICONTROL MMP]**：指定公司已啟用使用 [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP])功能。 此 [!UICONTROL MMP] 允許使用在Experience Cloud間共用對象 [!UICONTROL Experience Cloud ID] ([!DNL MCID])指派給每位訪客，然後由Audience Manager使用。 如果您選取此帳戶型別， [!UICONTROL Experience Cloud ID Service] 也會自動選取。

         如需詳細資訊，請參閱 [Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**：指定該公司為Audience Manager內的第三方資料提供者。
   * **[!UICONTROL Targeting Partner]**：指定公司作為Audience Manager客戶的目標平台。
   * **[!UICONTROL Visitor ID Service]**：指定公司已啟用使用 [!UICONTROL Experience Cloud Visitor ID Service].

      此 [!UICONTROL Experience Cloud Visitor ID Service] 提供跨Experience Cloud解決方案的通用訪客ID。 如需詳細資訊，請參閱 [Experience Cloud訪客ID服務使用手冊](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en).

   * **[!UICONTROL Agency]**：指定公司將擁有 [!UICONTROL Agency] 帳戶。



1. 按一下 **[!UICONTROL Create]**. 繼續下列中的指示： [編輯公司設定檔](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![步驟結果](assets/add_company.png)

## 編輯公司設定檔 {#edit-company-profile}

編輯公司的設定檔，包括其名稱、說明、子網域、生命週期等。

<!-- t_edit_company_profile.xml -->

1. 按一下 **[!UICONTROL Companies]**，然後找到並按一下所需的公司以顯示其 [!UICONTROL Profile] 頁面。

   使用 [!UICONTROL Search] 方塊或清單底部的分頁控制項，以尋找所需的公司。 您可以按一下所需欄的標頭，以遞增或遞減順序排序每個欄。

   ![步驟結果](assets/profile_company.png)

1. 視需要編輯欄位:

   * **[!UICONTROL Name]**：編輯公司名稱。 此為必填欄位。
   * **[!UICONTROL Description]**：編輯公司的說明。 此為必填欄位。
   * **[!UICONTROL Subdomain]**：（必要）指定公司的子網域。 您輸入的文字會顯示為事件呼叫的子網域。 無法變更此設定。 它必須是字串 [!DNL URL] — 有效字元。

      例如，如果貴公司名為 [!DNL AcmeCorp]，子網域會是 [!DNL acmecorp].

      Audience Manager會將子網域用於 [!UICONTROL Data Collection Server] (DCS)。 在上一個範例中，如果您的公司已滿 [!DNL URL] 在 [!UICONTROL DCS] 會是 [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**： ([!UICONTROL Identity Management System Organization ID])此ID可讓您將您的公司與Adobe Experience Cloud連線。
   * **[!UICONTROL Lifecyle]**：指定公司需要的階段：
      * **[!UICONTROL Active]**：指定該公司將成為作用中Audience Manager使用者端。 有效帳戶是指付款客戶，不僅是為了諮詢，也是為了提供Audience ManagerSKU。
      * **[!UICONTROL Demo]**：指定公司僅供示範用途。 系統會自動偽造報表資料。
      * **[!UICONTROL Prospect]**：指定該公司是潛在的Audience Manager客戶，例如可免費使用的公司 [!DNL POC] 或銷售示範的帳戶設定。
      * **[!UICONTROL Test]**：指定公司僅供內部測試之用。
   * **[!UICONTROL Account Types]**：指定此公司的完整帳戶型別集。 沒有帳戶型別與任何其他型別互斥。
      * **[!UICONTROL Full AAM]**：指定公司將擁有完整的Adobe Audience Manager帳戶，且使用者將擁有登入存取權。
      * **[!UICONTROL MMP]**：指定公司已啟用使用主要行銷設定檔([!UICONTROL MMP])功能。

         如果您選取此帳戶型別， **[!UICONTROL Visitor ID Service]** 也會自動選取。
如需詳細資訊，請參閱 [Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**：指定該公司為Audience Manager內的第三方資料提供者。
   * **[!UICONTROL Targeting Partner]**：指定公司作為Audience Manager客戶的目標平台。
   * **[!UICONTROL Visitor ID Service]**：指定公司已啟用使用Experience Cloud訪客ID服務。

      Experience Cloud 訪客 ID 服務提供跨 Experience Cloud 解決方案的通用訪客 ID。如需詳細資訊，請參閱 [Experience CloudID服務使用手冊](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en).

   * **[!UICONTROL Agency]**：指定公司將擁有Agency帳戶。
   * **[!UICONTROL Features]**: 選擇所要的選項:
      * **[!UICONTROL Password Expiration]**：設定該公司內的所有使用者密碼在90天後過期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**：為此公司啟用Audience Manager報告。
      * **[!UICONTROL Role Based Access Controls]**：啟用此公司的角色型存取控制。 角色型存取控制可讓您建立具有不同存取許可權的使用者群組。 之後，這些群組中的個別使用者只能存取Audience Manager中的特定功能。


1. 按一下 **[!UICONTROL Submit Updates]**.

## 刪除公司設定檔 {#delete-company-profile}

使用 [!UICONTROL Companies] Audience Manager中的頁面 [!UICONTROL Admin] 工具來刪除現有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必須擁有 [!UICONTROL DEXADMIN] 角色以刪除現有公司。

1. 若要刪除現有公司，請按一下 **[!UICONTROL Companies]**.

   ![步驟結果](assets/companies.png)

1. 按一下  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 欄中的所需公司。
1. 按一下 **[!UICONTROL OK]** 以確認刪除。
