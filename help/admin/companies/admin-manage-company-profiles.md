---
description: 使用「Audience Manager管理」工具中的「公司」頁可以建立新公司。
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

使用 [!UICONTROL Companies] 的子菜單。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必須 **[!UICONTROL DEXADMIN]** 角色以建立新公司。

1. 按一下 **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. 填寫欄位: 

   * **[!UICONTROL Name]**:（必需）指定公司名稱。
   * **[!UICONTROL Description]**:（必需）提供有關公司的描述性資訊，如行業或公司全名。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。 您輸入的文本顯示為事件調用的子域。 不能更改。 它必須是 [!DNL URL] — 有效字元。

      例如，如果您的公司被命名 [!DNL AcmeCorp]，子域 [!DNL acmecorp]。

      Audience Manager使用子域 [!UICONTROL Data Collection Server] (DCS)。 在上例中，如果您的公司 [!DNL URL] 在 [!UICONTROL DCS] 會 [!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**:指定公司所需的階段：
      * **[!UICONTROL Active]**:指定公司將是活動Audience Manager客戶端。 安 [!UICONTROL Active] 客戶是指付費客戶，不僅用於咨詢，還用於Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司僅用於演示。 報告資料將自動偽造。
      * **[!UICONTROL Prospect]**:指定公司是潛在Audience Manager客戶，如獲得免費服務的公司 [!DNL POC] 或銷售演示的帳戶設定。
      * **[!UICONTROL Test]**:指定公司僅用於內部測試。
   * **[!UICONTROL Account Types]**:指定此公司的完整帳戶類型集。 任何帳戶類型與任何其他類型互斥。
      * **[!UICONTROL Full AAM]**:指定公司將擁有完整的Adobe Audience Manager帳戶，用戶將擁有登錄訪問權限。
      * **[!UICONTROL MMP]**:指定公司已啟用，以使用 [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP])功能。 的 [!UICONTROL MMP] 允許觀眾使用 [!UICONTROL Experience Cloud ID] ([!DNL MCID])，分配給每個訪問者，然後由Audience Manager使用。 如果選擇此帳戶類型， [!UICONTROL Experience Cloud ID Service] 的子菜單。

         有關詳細資訊，請參見 [Experience Cloud觀眾](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager內的第三方資料提供程式。
   * **[!UICONTROL Targeting Partner]**:指定公司充當Audience Manager客戶的目標平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已啟用，以使用 [!UICONTROL Experience Cloud Visitor ID Service]。

      的 [!UICONTROL Experience Cloud Visitor ID Service] 提供跨Experience Cloud解決方案的通用訪問者ID。 有關詳細資訊，請參見 [Experience Cloud訪問者ID服務使用手冊](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en)。

   * **[!UICONTROL Agency]**:指定公司將 [!UICONTROL Agency] 帳戶。



1. 按一下 **[!UICONTROL Create]**. 繼續中的說明 [編輯公司配置檔案](../companies/admin-manage-company-profiles.md#edit-company-profile)。

   ![步驟結果](assets/add_company.png)

## 編輯公司設定檔 {#edit-company-profile}

編輯公司的配置檔案，包括其名稱、說明、子域、生命週期等。

<!-- t_edit_company_profile.xml -->

1. 按一下 **[!UICONTROL Companies]**，然後找到並按一下所需的公司以顯示其 [!UICONTROL Profile] 的子菜單。

   使用 [!UICONTROL Search] 或清單底部的分頁控制項，以查找所需的公司。 通過按一下所需列的標題，可以按升序或降序對每列進行排序。

   ![步驟結果](assets/profile_company.png)

1. 視需要編輯欄位:

   * **[!UICONTROL Name]**:編輯公司名稱。 這是必填欄位。
   * **[!UICONTROL Description]**:編輯公司說明。 這是必填欄位。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。 您輸入的文本顯示為事件調用的子域。 不能更改。 它必須是 [!DNL URL] — 有效字元。

      例如，如果您的公司被命名 [!DNL AcmeCorp]，子域 [!DNL acmecorp]。

      Audience Manager使用子域 [!UICONTROL Data Collection Server] (DCS)。 在上例中，如果您的公司 [!DNL URL] 在 [!UICONTROL DCS] 會 [!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**:([!UICONTROL Identity Management System Organization ID])此ID允許您將公司與Adobe Experience Cloud連接。
   * **[!UICONTROL Lifecyle]**:指定公司所需的階段：
      * **[!UICONTROL Active]**:指定公司將是活動Audience Manager客戶端。 活動帳戶是指付費客戶，不僅用於咨詢，還用於Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司僅用於演示。 報告資料將自動偽造。
      * **[!UICONTROL Prospect]**:指定公司是潛在Audience Manager客戶，如獲得免費服務的公司 [!DNL POC] 或銷售演示的帳戶設定。
      * **[!UICONTROL Test]**:指定公司僅用於內部測試。
   * **[!UICONTROL Account Types]**:指定此公司的完整帳戶類型集。 任何帳戶類型與任何其他類型互斥。
      * **[!UICONTROL Full AAM]**:指定公司將擁有完整的Adobe Audience Manager帳戶，用戶將擁有登錄訪問權限。
      * **[!UICONTROL MMP]**:指定公司已啟用使用主市場營銷配置檔案([!UICONTROL MMP])功能。

         如果選擇此帳戶類型， **[!UICONTROL Visitor ID Service]** 的子菜單。
有關詳細資訊，請參見 [Experience Cloud觀眾](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager內的第三方資料提供程式。
   * **[!UICONTROL Targeting Partner]**:指定公司充當Audience Manager客戶的目標平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已啟用以使用Experience Cloud訪問者ID服務。

      Experience Cloud 訪客 ID 服務提供跨 Experience Cloud 解決方案的通用訪客 ID。有關詳細資訊，請參見 [Experience CloudID服務使用手冊](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)。

   * **[!UICONTROL Agency]**:指定公司將具有代理帳戶。
   * **[!UICONTROL Features]**: 選擇所要的選項:
      * **[!UICONTROL Password Expiration]**:將此公司內的所有用戶密碼設定為90天後過期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**:啟用此公司的Audience Manager報告。
      * **[!UICONTROL Role Based Access Controls]**:為此公司啟用基於角色的訪問控制。 基於角色的訪問控制允許您建立具有不同訪問權限的用戶組。 然後，這些組中的單個用戶只能訪問Audience Manager中的特定功能。


1. 按一下 **[!UICONTROL Submit Updates]**.

## 刪除公司配置檔案 {#delete-company-profile}

使用 [!UICONTROL Companies] 頁面的Audience Manager [!UICONTROL Admin] 工具以刪除現有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必須 [!UICONTROL DEXADMIN] 角色以刪除現有公司。

1. 要刪除現有公司，請按一下 **[!UICONTROL Companies]**。

   ![步驟結果](assets/companies.png)

1. 按一下  ![](assets/icon_delete.png) 的 **[!UICONTROL Actions]** 列。
1. 按一下 **[!UICONTROL OK]** 確認刪除。
