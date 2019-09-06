---
description: 列出您可用來建立FTP資料檔案的巨集。有些巨集可用於所有資料檔案欄位和列。其他巨集僅適用於標題和資料行。
seo-description: 列出您可用來建立FTP資料檔案的巨集。有些巨集可用於所有資料檔案欄位和列。其他巨集僅適用於標題和資料行。
seo-title: 檔案格式巨集
title: 檔案格式巨集
uuid: f91c91b6-6581-4ed7-8d7f-f8532 bd41 df9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# 檔案格式巨集 {#file-format-macros}

列出您可用來建立 [!DNL FTP]型資料檔案的巨集。有些巨集可用於所有資料檔案欄位和列。其他巨集僅適用於標題和資料行。

## 通用巨集 {#common-macros}

這些巨集可用於任何格式欄位。如需範例，請參閱 [檔案格式巨集範例](../formats/file-format-examples.md)。

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_ SOH</code> </p> </td> 
   <td colname="col2"> <p>非列印ASCII字元。它表示一列或一個內容區段的開頭。它也可以用來分隔檔案中的資料欄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>目標資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_ DPID</code> </p> </td> 
   <td colname="col2"> <p>使用者ID金鑰資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p>訂單/目的地ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALAS</code> </p> </td> 
   <td colname="col2"> <p>訂單/目的地ID的別名。 </p> <p>此別名的「 <span class="wintitle"> 國外帳戶ID </span> 」欄位中設定此別名的值(在 <span class="wintitle"> 「基本設定 </span> 」區段中)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>同步_ MODE</code> </p> </td> 
   <td colname="col2"> <p>指出同步類型。接受下列可選變數： </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>完整</code>：完全同步。 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>ier</code>：漸進式同步。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>同步_類型</code> </p> </td> 
   <td colname="col2"> <p>表示資料傳輸方法。接受下列可選變數： </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>時間戳記</code> </p> </td> 
   <td colname="col2"> <p>10位數、UTC、Unix時間戳記。 </p> <p>它也可以設定為 <code>yyYYMMDDHMSS，AyyYMMDDHMSS採用</code> Java日期/時間戳記格式規則。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標題欄位巨集 {#header-field-macros}

僅用於標題欄位的巨集。如需範例，請參閱 [檔案格式巨集範例](../formats/file-format-examples.md)。

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>作為分隔符號，此巨集會在欄位之間插入標籤。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 資料行巨集 {#data-row-macros}

僅用於資料行的巨集。如需範例，請參閱 [檔案格式巨集範例](../formats/file-format-examples.md)。

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CONTRY_ CLUEY_ CASTAR</code> </p> </td> 
   <td colname="col2"> <p>插入封閉的大括號}字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMA</code> </p> </td> 
   <td colname="col2"> <p>插入逗號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> 資料合作夥伴唯一使用者識別碼 </span>。傳回您已將該ID與 <span class="keyword"> Audience Manager </span> 裝置ID同步時指派給使用者/網站訪客的ID。 </p> <p>如果DPID為0，此巨集會傳回 <span class="keyword"> Audience Manager </span> ID，而非使用者的ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID_ LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回包含資料合作夥伴多個ID的清單。如果您擁有一個大型組織，具有多個分部或其他可與您共用資料的組織群組，這個情況很有用。此巨集會傳回這些下屬群組的ID清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUID</code> </p> </td> 
   <td colname="col2"> <p>此巨集的輸出會將資料提供者ID(DPID)對應至相關的唯一使用者ID(DPUUID)。此巨集必須具有格式字串，才能控制其輸出。範例輸出看起來類似下列： </p> <p> <code>「dpids= dpid1，dpid2，… dpid n| maxMapTypes= n| format= json」</code> </p> <p><code>maxMapping</code> 設定會決定您希望巨集傳回多少映射。<code>當maxMATPapping=0</code>時，此巨集會傳回每個指定DPID的所有對應。資料會按照時間戳記(最近一個)排序，並傳回具有最大時間戳記的結果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>使用條件式 <code>時</code> ，若 <code>與SLOPE_ LIST</code> 和 <code>REMOVED_ SERVER_ LIST</code> 巨集有所差異。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SESION_ LIST&amp;&amp; REEMENT_ SERGE_ LIST) endif</code> </p> </td> 
   <td colname="col2"> <p>此巨集組合會建立條件陳述式，列出使用者屬於 <i>並</i> 已移除的區段。如果兩個條件都未符合或沒有資料，它會傳回空字串。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Open_ Curly_ ASTAR</code> </p> </td> 
   <td colname="col2"> <p>插入一個開放的大括號{字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_ OUT</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。請勿使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Output_ Attribute_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。請勿使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Output_ Attribute_ Value</code> </p> </td> 
   <td colname="col2"> <p>傳回 <code>靜態</code> 、硬式編碼值1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>合作夥伴ID(PID)。PID會顯示在管理UI的 <span class="wintitle"> 「描述檔 </span> 」索引標籤下方。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>已移除_ SERGE_ LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回已移除的區段清單(如果有的話)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segment_ LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回清單中的區段清單。接受下列可選變數： </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>Segmentid</code>：舊版ID。不再提倡。使用 <code>sid</code> (僅限小寫)。 </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>：舊版ID。不再提倡。使用 <code>sid</code> (僅限小寫)。 </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>：區段ID。 </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>：傳回 <code>個</code>靜態硬碼值，將資料識別為區段資料。 </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>別名</code>：區段對應。不再提倡。使用 <code>sid</code> (僅限小寫)。 </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>laxpdateTime</code>：Unix時間戳記，指出上次區段的實現時間。 </li> 
    </ul> <p>將這些變數放入巨集後面的巨括號後面。例如，此程式碼會將結果與垂直號分隔」|「字元： <code>&lt; SERGE_ LIST：{seg|&lt; seg. type&gt;，&lt; seg. sid&gt;}；separator=」|「&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ TICETS</code> </p> </td> 
   <td colname="col2"> <p>傳回 <code>靜態</code> 、硬式編碼值1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>插入標籤分隔符號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回特性清單。接受下列選擇性引數： </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>：由數值ID識別的特徵類型。此變數傳回： 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>用於</code> 識別傳入工作的DPM特徵(離線、上線)。 </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3，識別</code> 規則型特徵(即時、透過 <span class="wintitle"> DCS </span>註冊)。 </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>TraiID</code>：特徵ID。 </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>已實現</code>：最後一次實現特徵。Unix時間戳記。 </li> 
    </ul> <p>將這些變數放入巨集後面的巨括號後面。例如，此程式碼會將結果與垂直號分隔。|「字元： <code>TRAIT_ LIST{type| TratiId}；separator=」|」</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> 使用者ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>