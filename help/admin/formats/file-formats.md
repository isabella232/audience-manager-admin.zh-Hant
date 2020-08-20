---
description: 列出可用於建立基於FTP的資料檔案的宏。 某些宏可用於所有資料檔案欄位和行。 其他宏僅特定於標題行和資料行。
seo-description: 列出可用於建立基於FTP的資料檔案的宏。 某些宏可用於所有資料檔案欄位和行。 其他宏僅特定於標題行和資料行。
seo-title: 檔案格式巨集
title: 檔案格式巨集
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 2%

---


# 檔案格式巨集 {#file-format-macros}

列出可用於建立基於資料文 [!DNL FTP]件的宏。 某些宏可用於所有資料檔案欄位和行。 其他宏僅特定於標題行和資料行。

## 常見宏 {#common-macros}

這些宏可用於任何格式欄位。 如需範例，請參 [閱檔案格式巨集範例](../formats/file-format-examples.md)。

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
   <td colname="col2"> <p>非列印ASCII字元。 它指示行或內容部分的開始。 它也可用來分隔檔案中的資料欄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>目標資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>使用者ID金鑰資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>訂單／目標ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>訂單／目標ID的別名。 </p> <p>此別名的值會設定在目標的 <span class="wintitle"> Foerign Account ID(外 </span> 來帳戶ID)欄位中(在 <span class="wintitle"> Basic Settings（基本設定） </span> 區段)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>表示同步類型。 接受下列可選變數： </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>:完全同步。 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>:增量同步。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>表示資料傳輸方法。 接受下列可選變數： </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>10位數的UTC、Unix時間戳記。 </p> <p>也可以按照Java日期／時 <code>YYYYMMDDhhmmss</code> 間戳格式規則進行格式化。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標題欄位巨集 {#header-field-macros}

僅用於標題欄位的宏。 如需範例，請參 [閱檔案格式巨集範例](../formats/file-format-examples.md)。

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
   <td colname="col2"> <p>此巨集用作分隔符號，可在欄位之間插入索引標籤。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 資料列巨集 {#data-row-macros}

僅用於資料行的宏。 如需範例，請參 [閱檔案格式巨集範例](../formats/file-format-examples.md)。

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
   <td colname="col2"> <p>插入一個右括弧 <code>}</code> 字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>插入逗號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> 資料合作夥伴唯一使用者識別 </span>碼。 傳回您指派給使用者／網站訪客的ID(如果該ID已與 <span class="keyword"></span> Audience Manager裝置ID同步)。 </p> <p>如果DPID為0，此巨集會傳回 <span class="keyword"> Audience Manager </span> ID，而非您的ID給使用者。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回包含資料合作夥伴多個ID的清單。 如果您有一個大型組織，其中包含多個子組織或允許您與其共用資料的其他組織組，則此功能非常有用。 此巨集會傳回這些附屬群組的ID清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>此巨集的輸出會將資料提供者ID(DPID)對應至相關的唯一使用者ID(DPUUID)。 此宏必須具有格式字串才能控制其輸出。 範例輸出看起來類似下列： </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>設 <code>maxMappings</code> 置確定要返回宏的映射數。 當 <code>maxMappings=0</code>時，此宏返回每個指定DPID的所有映射。 資料會依時間戳記（最新的先行）排序，並傳回最大時間戳記優先的結果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>使用條件和宏 <code>if</code> 和宏 <code>SEGMENT_LIST</code> 時需 <code>REMOVED_SEGMENT_LIST</code> 要。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>此宏組合會建立條件語句，列出用戶屬於和已 <i>從</i> 中刪除的段。 如果兩個條件都不符合或沒有資料，則會傳回空字串。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud ID.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>插入一個左括弧 <code>{</code> 字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。請勿使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。請勿使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>傳回 <code>1</code> 為靜態、硬式編碼值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>合作夥伴ID(PID)。 PID會顯示在管理員UI <span class="wintitle"> 的「 </span> 設定檔」標籤下。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回已移除的區段清單（如果有）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回清單中的區段清單。 接受下列可選變數： </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>:舊版ID。 不再提倡。使 <code>sid</code> 用（僅小寫）。 </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>:舊版ID。 不再提倡。使 <code>sid</code> 用（僅小寫）。 </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>:區段ID。 </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>:傳回 <code>5</code>靜態、硬式編碼值，將資料識別為區段資料。 </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>:區段的對應。 不再提倡。使 <code>sid</code> 用（僅小寫）。 </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>:Unix時間戳記，指示上次實現段的時間。 </li> 
    </ul> <p>將這些變數放在巨集後面的大括弧中。 例如，此程式碼會以垂直號"|"字元分隔結果： <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>傳回 <code>1</code> 為靜態、硬式編碼值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>插入制表符分隔符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回特徵清單。 接受以下可選參數： </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>:由數值ID識別的特徵類型。 此變數會傳回： 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> 識別DPM特徵（離線，由傳入工作加入）。 </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> 識別基於規則的特徵(即時、已透過 <span class="wintitle"> DCS </span>登入)。 </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>:特徵ID。 </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>:上次這個特徵被發現。 Unix時間戳記。 </li> 
    </ul> <p>將這些變數放在巨集後面的大括弧中。 例如，此程式碼會以垂直號"|"字元分隔結果： <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager使 </span> 用者ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>