---
description: 'null'
seo-description: 'null'
seo-title: 使用粗細篩選
solution: Experience Manager
title: 使用粗細篩選
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用粗細篩選{#using-the-profanity-filter}

所有張貼至Livefyre應用程式的內容都會被檢查為褻瀆。 如果內容或使用者的顯示名稱中發現包含在粗體清單中的字詞，該內容會標示為「粗體」，讓您可以篩選該字詞以用於「預協調」、「規則」、「ModQ」或「應用程式內容」中的一般搜尋。

>[!NOTE]
>
>Studio管理員和經理的內容不受「粗細規則」檢查的約束，協調者張貼的內容也不會被標幟。

Livefyre提供預設的剖析清單。 您可以選擇在網路層級套用此清單、提供您自己的清單，或使用兩者的匯總。 您網路中的各個站點可能繼承網路「Profity List」，或者使用自定義為特定於站點的清單。

若要提供您自己的自訂描述檔清單作為網路預設值，請將它傳送至您的Livefyre帳戶管理員。

## 啟用剖析篩選 {#section_yqc_qsk_f1b}

在網路和網站層級啟用並設定profanity篩選。 在網路層級停用profity篩選，自動停用從網路繼承的所有網站的profity篩選。

>[!NOTE]
>
>所有透過Livefyre傳遞的內容都會檢查為否有褻瀆。 如果找到包含預設SAFE描述檔清單或自訂描述檔清單中所包含之字詞的內容，則會標示為「Profinity」。若要設定Livefyre自動對這些項目採取動作，請轉 **[!UICONTROL Enable Profanity Checking]** 至 **[!UICONTROL ON]**。

## 為網路啟用「屬性過濾器」 {#section_twd_ssk_f1b}

1. 從網 **[!UICONTROL Network]** 絡下拉菜單中選擇。
1. 前往 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 向下滾動到 **[!UICONTROL Profanity List]**，並設定 **[!UICONTROL Enable Profanity Checking]** 為 **[!UICONTROL ON]**。

1. 使用欄 **[!UICONTROL Update Network Profanity List]** 位將字詞新增至清單，或按一下字詞將其從清單中移除。

>[!NOTE]
>
>編輯網路層級的「專業性清單」不會影響任何已建置的網站層級清單。 為確保對站點進行網路更改，請在 **[!UICONTROL Restore Network List]** 進行更改後為站點選擇。

## 啟用網站的「屬性篩選」 {#section_fld_wsk_f1b}

1. 從網路下拉菜單中選擇站點。
1. 前往 **[!UICONTROL Settings > Site Settings > Moderation]**.
1. 向下滾動到 **[!UICONTROL Profanity List]** 並設定 **[!UICONTROL Enable Profanity Checking]** 為 **[!UICONTROL ON]**。

1. 選擇下列選項之一：

   * 要從網路繼承Profity List（這不常見），請設定 **[!UICONTROL Use Site Profanity List]** 為 **[!UICONTROL OFF]**。

   * 若要特別編輯網站的「剖析清單」, **[!UICONTROL Use Site Profanity List]** 請設 **[!UICONTROL On]** 定為開 **[!UICONTROL Update Profanity List]** 啟欄位，您可在其中編輯清單：

      * 若要移除字詞，請按一下該字詞。
      * 若要新增字詞，請在方塊中輸入該 **[!UICONTROL Add new word]** 字詞並點擊 **[!UICONTROL Return]**。

      * 若要查看清單中是否包含字詞，請在方塊中輸入該 **[!UICONTROL Test profanity filter]** 字詞。
   * 若要重新匯入網路「Profity List」並將它套用至網站，請按一下 **[!UICONTROL Restore Network List]**。
   * 若要清除清單中的所有內容並從頭開始，請按一下 **[!UICONTROL Clear List]**。


## 使用包含褻瀆的內容 {#section_epy_dtk_f1b}

使用「Profity List」（屬性清單）協助篩選內容搜尋，並建立ModQ的「預先協調規則」。

若要搜尋包含粗體的內容，請前往 **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** 並勾選核取 **[!UICONTROL Profanity]** 方塊。 系統將顯示所選網站或網路的「屬性篩選」所擷取的所有內容。 此清單將包含使用SocialSync和串流提取至應用程式的內容。

若要建立預先協調規則，請從Studio選取 **[!UICONTROL Settings > Network Settings > Moderation]**。 一旦啟用了profity篩選，就會出現新規則，讓您可以標幟或預先協調包含profity的內容。 依預設，此規則會自動 **[!UICONTROL Premoderate]** 啟用剖析內容，可變更為 **[!UICONTROL Trash it]** 或 **[!UICONTROL Bozo it]**。

>[!NOTE]
>
>如果單一內容受多種規則類型（例如SAFE和Flag規則）約束，則會套用更嚴格的規則。 例如：如果您的「預先協調」規則指出要「預先協調內容」，但「安全」規則表示要「去垃圾」，則會「已清除」。

## 查看和更新網路的屬性清單 {#section_qdb_btk_f1b}

1. 前往 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 向下捲動至 **[!UICONTROL Profanity List]** 區段。
1. 設 **[!UICONTROL Enable Profanity Checking]** 為顯 **[!UICONTROL On]** 示您網路的「啟用清單」（預設值為Livefyre，或您上傳的自訂清單）並加以編輯。 您可以以下列方式編輯清單：
   * 若要移除字詞，請按一下該字詞。
   * 若要新增字詞，請在方塊中輸入該 **[!UICONTROL Add new word]** 字詞並點擊 **[!UICONTROL Return]**。
   * 若要查看清單中是否包含字詞，請在方塊中輸入該 **[!UICONTROL Test profanity filter]** 字詞。

>[!NOTE]
>
>只有Studio管理員和協調者才能編輯Profity Lists。

