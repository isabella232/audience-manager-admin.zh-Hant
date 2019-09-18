---
description: 依日期列出Audience Manager管理指南的所有更新（新增、刪除和更正）。
seo-description: 依日期列出Audience Manager管理指南的所有更新（新增、刪除和更正）。
seo-title: 文件更新
title: 文件更新
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
translation-type: tm+mt
source-git-commit: e60aa0ac341d74454bfe00a4f56add3a9f9e281b

---


# 文件更新 {#documentation-updates}

依日期列出Audience Manager管理指南的所有更新（新增、刪除和更正）。

如需功能發行、增強功能和錯誤修正的詳細資訊，請參閱 [Experience cloud發行說明](https://marketing.adobe.com/resources/help/en_US/whatsnew/)。 請參閱[之前的發行說明](https://marketing.adobe.com/resources/help/en_US/whatsnew/c_legacy_releases.html)瞭解以往的 Experience Cloud 公告。如需文 [!DNL Audience Manager documentation changes, see] 件 [更新](https://docs.adobe.com/content/help/en/audience-manager/user-guide/documentation-updates/docs-2019.html)。

## AAM 2019檔案更新 {#aam-2019-docs-updates}


| 主題 | 說明 |
---------|----------|
| HTTP格式宏 | 我們為宏添加了新 `REGION_ID_LIST`的宏`sda`、`sda`、和 `sda` 三個新欄位 `USER_LIST` 。 |
| HTTP格式宏 | 我們新增了兩個巨集： `ECID` 和 `MCID`。 |


## AAM 2018檔案更新 {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> 建立或編輯FTP伺服器</a> </p> </td> 
   <td colname="col2"> <p>我們新增了有關SFTP伺服器的SSH金鑰驗證的詳細資訊（步驟5）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> 如何設定您的目的地以匯出Experience Cloud...</a> </p> </td> 
   <td colname="col2"> <p>此頁顯示如何設定目標以導出在出站資料檔案中要導出的ID類型的資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> 如何：授權批次目標的跨帳戶Amazon S3儲存桶訪問</a> </p> </td> 
   <td colname="col2"> <p>如果客戶不想共用Amazon S3存取金鑰和機密金鑰，可以使用Amazon S3中的跨帳戶儲存貯體權限來傳送傳出資料檔案。 本檔案會示範如何在Audience Manager管理員UI中設定此替代選項。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017檔案更新 {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP格式宏</a> </td> 
   <td colname="col2">以legacySegmentId <code>取代</code> segmentId <code>巨集，並新增</code> newSegmentId <code></code> macro。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6"> 管理公司限制</a> </td> 
   <td colname="col2"> 新增最大特徵資料夾數目和特徵結構深度至限制檔案。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> 啟用出站Hadoop序列檔案傳輸</a> </td> 
   <td colname="col2"> 瞭解如何讓客戶將出站SEQ檔案發送到自己的Hadoop實例。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> 管理容器</a> </td> 
   <td colname="col2"> 新增有關如何建立容器的簡短說明。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations"> 建立或編輯公司目標</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">已添加有關平衡使用完整同步和增量同步的說明。 </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7">將 <span class="keyword"> Adobe Media Optimizer布建為Audience Manager</span> (觀眾管理者 <span class="keyword"> )的目的地是在</span> Adobe Media Optimizer中完成 <span class="keyword"></span>。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目標</a> </p> </td> 
   <td colname="col2"> <p>小幅修訂。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> ID與Media Optimizer同步</a> </p> </td> 
   <td colname="col2"> <p>說明每個公司容器中AMO同步核取方塊的新檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> 適用於公司的裝置圖表選項</a> </p> </td> 
   <td colname="col2"> <p>說明如何設定裝置圖形選項的新檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> API需求與建議</a> </p> </td> 
   <td colname="col2"> <p>新檔案說明一些需要注意的要求和建議，並傳遞給客戶。 這會在具有相同標題的公開檔案中複製，並對不同閱讀對象進行變更。 請參 <a href="https://marketing.adobe.com/resources/help/en_US/aam/aam-api-requirements.html" format="https" scope="external"> 閱公開檔案中的</a> 「API需求與建議」。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016檔案更新 {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> 建立或編輯FTP伺服器</a> </td> 
   <td colname="col2">已新增出口FTP IP <b>52.44.29.204</b>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目標</a> </p> </td> 
   <td colname="col2"> <p>小幅修訂。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD"> 建立或編輯HTTP伺服器</a> </p> </td> 
   <td colname="col2"> <p>已將 <b>HTTP簽名新增至</b> 「建立伺服器設定」精靈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> 測試版環境</a> </p> </td> 
   <td colname="col2"> <p>在測試環境中更新URL和主機名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> 僅按活動用戶篩選出站資料</a> </p> </td> 
   <td colname="col2"> <p>生成僅包含活動用戶的完整同步檔案的說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP格式宏</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>列出HTTP巨集和常見範例的新檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式宏示例</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015檔案更新 {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2015年12月 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>已修訂巨集區段並新增範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014檔案更新 {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2014年11月12日 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>已新增有關&lt;MCID&gt;巨集的資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年10月23日 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> 建立或編輯格式</a> </p> </td> 
   <td colname="col2"> <p>已新增有關。info「收 <span class="wintitle"> 據」選項的 </span>資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年10月23日 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>新頁面。 請注意，本頁是進行中的工作，將在未來幾天內更新。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年10月22日 </p> <p><a href="admin-destination-troubleshooting.md#"> 目標設定疑難排解</a> </p> </td> 
   <td colname="col2"> <p> 新主題。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 21 日 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目標</a> </p> </td> 
   <td colname="col2"> <p>重寫了整個主題。已新增其他資訊和其他設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年9月25日 </p> <p><a href="companies/admin-manage-company-profiles.md"> 建立公司</a> </p> </td> 
   <td colname="col2"> <p>已新增其他資訊至「生命 <span class="wintitle"> 週期</span> 」和「 <span class="wintitle"> 帳戶類型</span> 」區段。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年9月25日 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> 編輯公司設定檔</a> </p> </td> 
   <td colname="col2"> <p>已新增其他資訊至「生命 <span class="wintitle"> 週期</span> 」和「 <span class="wintitle"> 帳戶類型</span> 」區段。 </p> </td> 
  </tr> 
 </tbody> 
</table>