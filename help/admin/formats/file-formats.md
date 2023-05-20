---
description: 列出可用於建立基於FTP的資料檔案的宏。 某些宏可用於所有資料檔案欄位和行。 其他宏僅特定於標題行和資料行。
seo-description: Lists the macros you can use to create FTP-based data files. Some macros can be used for all data file fields and rows. Other macros are specific to header and data rows only.
seo-title: File Format Macros
title: 檔案格式巨集
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
exl-id: e686bc33-da3e-49a9-8c71-2bc6ca399bfb
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 2%

---

# 檔案格式巨集 {#file-format-macros}

列出可用於建立的宏 [!DNL FTP]基於的資料檔案。 某些宏可用於所有資料檔案欄位和行。 其他宏僅特定於標題行和資料行。

## 通用宏 {#common-macros}

這些宏可用於任何格式欄位。 有關示例，請參見 [檔案格式宏示例](../formats/file-format-examples.md)。

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>非打印ASCII字元。 它指示行或內容部分的開始。 它還可用於分隔檔案中的資料列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>目標資料提供程式ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>用戶ID密鑰資料提供程式ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>訂單/目標ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>訂單/目標ID的別名。 </p> <p>此別名的值在 <span class="wintitle"> 外來帳戶ID </span> 目標的欄位(在 <span class="wintitle"> 基本設定 </span> )的正平方根。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>指示同步類型。 接受以下可選變數： </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>:完全同步。 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>:增量同步。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>指示資料傳輸方法。 接受以下可選變數： </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>10位UTC、Unix時間戳。 </p> <p>也可以將其格式化為 <code>YYYYMMDDhhmmss</code> 遵循Java日期/時間戳格式設定規則。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標題欄位宏 {#header-field-macros}

僅在標題欄位中使用的宏。 有關示例，請參見 [檔案格式宏示例](../formats/file-format-examples.md)。

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>此宏用作分隔符，在欄位之間插入一個制表符。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 資料行宏 {#data-row-macros}

僅在資料行中使用的宏。 有關示例，請參見 [檔案格式宏示例](../formats/file-format-examples.md)。

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>插入右花括弧 <code>}</code> 字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>插入逗號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> 資料合作夥伴唯一用戶標識符 </span>。 如果用戶/站點訪問者的ID已與 <span class="keyword"> Audience Manager </span> 設備ID。 </p> <p>如果DPID為0，則此宏將返回 <span class="keyword"> Audience Manager </span> 用戶的ID而不是ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回包含資料夥伴的多個ID的清單。 如果您有一個大型組織，具有多個子部門或允許您與其共用資料的其他組織組，則此功能非常有用。 此宏返回這些從屬組的ID清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>此宏的輸出將資料提供程式ID(DPID)映射到相關的唯一用戶ID(DPUUID)。 此宏必須具有格式字串才能控制其輸出。 示例輸出將與以下內容類似： </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>的 <code>maxMappings</code> 設定確定希望宏返回的映射數。 當 <code>maxMappings=0</code>，此宏返回每個指定DPID的所有映射。 資料按時間戳（最新的第一個）排序，並返回最大時間戳的結果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>使用條件時必需 <code>if</code> 和 <code>SEGMENT_LIST</code> 和 <code>REMOVED_SEGMENT_LIST</code> 宏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>此宏組合會建立一個條件語句，列出用戶所屬的段 <i>和</i> 已從中刪除。 如果兩個條件都未滿足或沒有資料，則返回空字串。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud ID.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>插入左花括弧 <code>{</code> 字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。別用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。別用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>返回 <code>1</code> 作為靜態硬編碼值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>合作夥伴ID(PID)。 PID出現在 <span class="wintitle"> 配置檔案 </span> 頁籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回已刪除的段（如果有）的清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回清單中段的清單。 接受以下可選變數： </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>:舊ID。 不再提倡。使用 <code>sid</code> （僅小寫）。 </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>:舊ID。 不再提倡。使用 <code>sid</code> （僅小寫）。 </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>:段ID。 </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>:返回 <code>5</code>，一個靜態的硬編碼值，它將資料標識為段資料。 </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>:段的映射。 不再提倡。使用 <code>sid</code> （僅小寫）。 </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>:一個Unix時間戳，指示上次實現段的時間。 </li> 
    </ul> <p>將這些變數放在宏後面的大括弧中。 例如，此代碼將結果與管道「|」字元分隔： <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>返回 <code>1</code> 作為靜態硬編碼值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>插入制表符分隔符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回特徵清單。 接受以下可選參數： </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>:由數字ID標識的特性類型。 此變數返回： 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> 標識DPM特性（離線，由入站作業掛接）。 </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> 識別基於規則的特徵(即時、穿過 <span class="wintitle"> DCS </span>)。 </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>:特徵ID </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>:上次這個特徵被發現。 Unix時間戳。 </li> 
    </ul> <p>將這些變數放在宏後面的大括弧中。 例如，此代碼用管道「|」字元分隔結果： <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> 用戶ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>
