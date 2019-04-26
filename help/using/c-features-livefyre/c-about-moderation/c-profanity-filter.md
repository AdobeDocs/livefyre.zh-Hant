---
description: null
seo-description: null
seo-title: 使用嚴格篩選
solution: Experience Manager
title: 使用嚴格篩選
uuid: b0b1fbae-c88 c-403c-9b91-df61620675 f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用嚴格篩選{#using-the-profanity-filter}

所有張貼到Livefyre應用程式中的內容都會受到褻瀆。如果「粗話」清單中包含的字詞出現在內容中或使用者的顯示名稱中，則該內容會被標示為「褻瀆」，讓您篩選其「Premiere」、「規則」、「ModQ」或「App Content」中的一般搜尋。

>[!NOTE]
>
>Studio管理員和經理的內容不受「褻瀆規則」檢查，並不會標幟由協調者張貼的內容。

Livefyre提供預設的字詞清單。您可以選擇在網路層級套用此清單、提供自己的清單或使用兩者的匯總。網路內的個別網站可能會繼承網路「褻瀆清單」，或使用自訂為網站特定的清單。

若要提供您自己的自訂粗俗清單作為網路預設，請將它傳送給您的Livefyre帳戶管理員。

## 啓用褻瀆篩選 {#section_yqc_qsk_f1b}

啓用並設定網路和網站層級的嚴格篩選。停用網路層級的粗性篩選，自動停用所有繼承自網路之網站的粗性篩選。

>[!NOTE]
>
>所有通過Livefyre的內容都會受到褻瀆。如果發現包含預設SAFE粗話清單或您自訂「褻瀆」清單中的字詞的內容，會標示為「褻瀆」。」若要設定Livefyre以自動對這些項目執行動作，請改用 **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**。

## 為網路啓用嚴格篩選 {#section_twd_ssk_f1b}

1. **[!UICONTROL Network]** 從網路下拉式選單中選取。
1. **[!UICONTROL Settings > Network Settings > Moderation]**前往。
1. 向下捲動至， **[!UICONTROL Profanity List]**然後設 **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**為。

1. 使用 **[!UICONTROL Update Network Profanity List]** 欄位新增單字至清單，或按一下單字將它從清單中移除。

>[!NOTE]
>
>編輯網路層級「褻瀆清單」不會影響任何網站層級清單。為確保網站對網站進行變更，請在 **[!UICONTROL Restore Network List]** 變更完成後選取網站。

## 為網站啓用嚴格篩選 {#section_fld_wsk_f1b}

1. 從網路下拉式選單選取網站。
1. **[!UICONTROL Settings > Site Settings > Moderation]**前往。
1. 向下捲動至並 **[!UICONTROL Profanity List]** 設 **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**為。

1. 選擇下列其中一個選項：

   * 若要繼承網路(此並非一般)的「褻瀆清單」，請設 **[!UICONTROL Use Site Profanity List]****[!UICONTROL OFF]**為。

   * 若要專門編輯網站的「褻瀆清單」，請設 **[!UICONTROL Use Site Profanity List]****[!UICONTROL On]** 為開啓 **[!UICONTROL Update Profanity List]** 欄位，供您編輯清單：

      * 若要移除單字，請按一下字詞。
      * To add a word, type the word into the **[!UICONTROL Add new word]** box and hit **[!UICONTROL Return]**.

      * 若要查看單字是否包含在清單中，請將字詞輸入 **[!UICONTROL Test profanity filter]** 方塊中。
   * 若要重新匯入網路褻瀆清單並將它套用至網站，請按一下 **[!UICONTROL Restore Network List]**。
   * 若要清除清單中的所有內容並從頭開始，請按一下 **[!UICONTROL Clear List]**。


## 使用包含Profanity的內容 {#section_epy_dtk_f1b}

使用「褻瀆清單」協助篩選您的內容搜尋，並建立ModQ的「預覽規則」。

若要搜尋包含粗性的內容，請前往 **[!UICONTROL Library > App Content]**並 **[!UICONTROL Filter by Flags]** 核取 **[!UICONTROL Profanity]** 核取方塊。將顯示所有被「嚴格篩選」所擷取之網站或網路的內容。此清單將包含使用SocialSync和Streams提取到應用程式中的內容。

若要建立「預覽」規則，請從Studio選取 **[!UICONTROL Settings > Network Settings > Moderation]**。一旦啓用嚴格篩選後，便會出現新規則，讓您可以「標幟」或「預覽」內容，以包含褻瀆內容。根據預設，此規則會自動啓用 **[!UICONTROL Premoderate]** 褻瀆內容，這些內容可能會變更為或 **[!UICONTROL Trash it]****[!UICONTROL Bozo it]**。

>[!NOTE]
>
>如果一部分內容受到多個規則類型(例如SAFE和Tradel規則)的約束，將會套用更嚴格的內容。例如：如果您的「預覽」規則顯示為「預先調節某一部分內容」，但「SAFE規則」表示「垃圾筒」，則會被毀壞。

## 檢視並更新網路的褻瀆清單 {#section_qdb_btk_f1b}

1. **[!UICONTROL Settings > Network Settings > Moderation]**前往。
1. 向下捲動至 **[!UICONTROL Profanity List]** 區段。
1. 設定 **[!UICONTROL Enable Profanity Checking]** 為 **[!UICONTROL On]** 顯示您網路的「清單」(Livefyre預設值或您已上載的自訂清單)並加以編輯。您可以透過下列方式編輯清單：
   * 若要移除單字，請按一下字詞。
   * To add a word, type the word into the **[!UICONTROL Add new word]** box and hit **[!UICONTROL Return]**.
   * 若要查看單字是否包含在清單中，請將字詞輸入 **[!UICONTROL Test profanity filter]** 方塊中。

>[!NOTE]
>
>只有Studio管理員和協調者才能編輯「褻瀆清單」。

