---
description: 列出您可用來建立HTTP資料檔案的巨集。HTTP會以JSON格式傳送資料。
seo-description: 列出您可用來建立HTTP資料檔案的巨集。HTTP會以JSON格式傳送資料。
seo-title: HTTP格式巨集
title: HTTP格式巨集
uuid: 91021f60-75d0-4b1d-86ca-91c9dadafac1
translation-type: tm+mt
source-git-commit: 1a547e421346a6bf281e2b3ff3a0bcb5cf1d78df

---


# HTTP格式巨集 {#http-format-macros}

列出您可用來建立 [!DNL HTTP] 資料檔案的巨集。[!DNL HTTP] 以 [!DNL JSON] 格式傳送資料。

如需一些常用巨集組合的清單和範例，請參閱 [HTTP格式巨集範例](../formats/web-format-examples.md) 。

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 方法類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>AAM_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> Audience Manager </span> ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>資料合作夥伴唯一使用者ID。如果使用者ID已與 <span class="keyword"> Audience Manager </span> 裝置ID同步，此巨集會傳回您指派給使用者的ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ECID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Generation_ Time</code> </p> </td> 
   <td colname="col2"> <p> <code>GET，POST</code> </p> </td> 
   <td colname="col3"> <p>Unix UTC時間戳記。內部時間戳記代表AAM收到通知，將 <span class="wintitle"> S </span> 目的地發佈給合作夥伴的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>使用者的IP位址。 </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID。(MCID代表Marketing Cloud，這是Experience Cloud的舊名稱) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ EXCEEMENT_ SERVES</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>使用者不再屬於的區段數(整數)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ SERSIONS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>使用者所屬區段的數目。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET，POST</code> </p> </td> 
   <td colname="col3"> <p>訂單或目的地ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET，POST</code> </p> </td> 
   <td colname="col3"> <p>合作夥伴ID的別名。也稱為「外國帳戶ID」。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>隨機</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>產生隨機數字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REASER_ ID_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>活動來源的 <a href="https://docs.adobe.com/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html"> Audience Manager DCS區域 </a> 。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>已移除_ SERGE_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>傳回使用者不再符合資格的區段ID清單(如果有的話)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>已移除_區段</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>使用者不再符合資格的區段清單。您也可以傳回特定區段欄位，其中包括： </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>TritialAS</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>LegacySegmentid(之前稱為SegmentiID)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>Newsegmentid</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>狀態</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>DateTime</code> </li> 
     </ul> </p> <p>在陣列中指定這些欄位，如本範例所示： </p> <p> <code>[&lt; REEMENT_ SERVER：{seg|&lt; OPEN_ CASTAR&gt;「對應」：&lt; seg. TritIalas&gt;，「狀態：「&lt; seg. status&gt;，」時間：&lt; seg. dateTime&gt;，「legacySegmentid」：&lt; seg. leaccysegEnd&gt;，「newsegmentid」：&lt; seg. NewsegMentid&gt;&lt; CLOSE_ ACCAR&gt;}；「separator=」，&gt;]</code> </p> <p>另請參閱 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式巨集範例 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REEMENT_ IMEY_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> 使用者不再符合資格的最後實作清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>已移除_ TRAITALIAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>使用者不再符合資格之別名的別名名稱清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segment_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>傳回區段ID清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>區段</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>使用者符合資格的區段清單。您也可以傳回特定區段欄位，其中包括： </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>TritialAS</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>LegacySegmentid(之前稱為SegmentiID)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>Newsegmentid</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>狀態</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>DateTime</code> </li> 
     </ul> </p> <p>在陣列中指定這些欄位，如本範例所示： </p> <p> <code>[&lt;區段：{seg|&lt; OPEN_ CASTAR&gt;「對應」：&lt; seg. TritIalas&gt;，「狀態：「&lt; seg. status&gt;，」時間：&lt; seg. dateTime&gt;，「legacySegmentid」：&lt; seg. leaccysegEnd&gt;，「newsegmentid」：&lt; seg. NewsegMentid&gt;&lt; CLOSE_ ACCAR&gt;}；「separator=」，&gt;]</code> </p> <p>另請參閱 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式巨集範例 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Time_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>最後實作的清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>時間戳記</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Unix，UTC時間戳記。代表區段的最後實作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TraITALIAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>特定區段的別名名稱清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>User_ Agent</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>初始請求的使用者代理。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p><span class="keyword"> Audience Manager </span> 使用者ID清單。您也可以傳回包含下列項目的特定欄位： </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user. aamuId</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user. dpuuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user. segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user. removedSegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user. userAgent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user. ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user. dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user. timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user. random</code> </li>
     <li><code>user. regionIDs</code></li> 
    </ul> <p>指定下列欄位，如此範例所示： </p> <p> 
     <codeblock>
       「AAM_ UUID」：「&lt; user. aamuId&gt;」DataAssaper_ UUID」：「&lt; user. dpuuid&gt;」 
     </codeblock> </p> <p>如需完整範例，請參閱 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式巨集範例 </a> 。 </p> </td> 
  </tr>
 </tbody>
</table>