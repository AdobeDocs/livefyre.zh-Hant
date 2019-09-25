---
description: 'null'
seo-description: 'null'
seo-title: Livefyre身分識別電子郵件
solution: Experience Manager
title: Livefyre身分識別電子郵件
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Livefyre身分識別電子郵件{#emails-for-livefyre-identity}

Livefyre Identity會傳送下列電子郵件：

* [密碼重設電子郵件](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [驗證電子郵件](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [傳送電子郵件驗證給使用者](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [歡迎電子郵件](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [傳送歡迎電子郵件給使用者](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

您可以自訂所有Livefyre身分識別電子郵件的外觀和感覺， **[!UICONTROL Integration Settings > Email Notifications.]**

## 密碼重設電子郵件 {#section_nd1_whs_p1b}

當使用者嘗試重設密碼時，Livefyre會自動傳送密碼重設電子郵件。

密碼重設電子郵件的外觀如下：

**** 主旨：重設密碼

**內文:**

嘿， *&lt;username&gt;*,

有人要求在&lt;網路名稱&gt;上更改配置 *式的密碼*。

如果您要求此密碼，請按一下下列連結以選擇新密碼： *&lt;密碼重設URL&gt;*。

*&lt;Username&gt;*、 *&lt;網路名稱&gt;*，以及 *&lt;密碼重設URL&gt;* ，都會根據網站訪客和您的網路動態產生。

## 驗證電子郵件 {#section_ak5_xhs_p1b}

您可以傳送電子郵件，驗證使用者的電子郵件地址。 若要傳送驗證電子郵件，您必須開啟「整合設定&gt; Livefyre **身分識別」中的選項**。

驗證電子郵件的外觀如下：

**** 主旨：電子郵件驗證

**內文:**

Hello *&lt;username&gt;*,

請按一下下列連結（或貼在您的瀏覽器中）以驗證您的帳戶： *&lt;驗證URL&gt;*。

此連結將於24小時內到期。

謝謝，

&lt;客 *戶名稱&gt;團隊*

*&lt;Username&gt;*、 *&lt;網路名稱&gt;*，以及 *&lt;驗證URL&gt;* ，都會根據網站訪客和您的網路動態產生。

## 傳送電子郵件驗證給使用者 {#section_vyv_yhs_p1b}

您可以傳送電子郵件給使用者，以驗證使用者用來註冊帳戶的電子郵件地址。 若要傳送驗證電子郵件：

1. 在Studio中，按一下齒輪圖示以修改網路設定。
1. 按一 **下「整合設定&gt; Livefyre Identity」。**

1. 導覽至登 **入類型**。
1. 按一 **下「要求電子郵件驗證** 」，傳送電子郵件給會驗證使用者用來註冊帳戶的電子郵件地址的使用者。
1. 導覽至「 **網路電子郵件** 」以設定「電子郵件」的 **標誌、用作寄件者地址(** Email From **)的電子郵件地址，以及用於寄件者電子郵件地址(****** Email Display Name Alignment)的顯示名稱。

## 歡迎電子郵件 {#section_z2v_zhs_p1b}

您可以傳送歡迎電子郵件給使用者。 若要傳送歡迎電子郵件，您必須開啟「整合設定 **&gt;** Livefyre身分識別」中的選項 ****。

歡迎電子郵件的外觀如下：

**** 主旨：歡迎使 *用&lt;客戶名稱&gt;*

**內文:**

Hello *&lt;username&gt;*,

已在&lt;客戶名稱&gt;上為您 *建立帳戶*。

此帳戶是在 *&lt;反向連結URL&gt;* ，從IP位 *址&lt;IP位址&gt;建立*。

如果您這麼做，您可以完全忽略此電子郵件。

如果您未執行此動作，請聯絡 `support@livefyre.com`

謝謝

「客 *戶名稱」團隊*

*「使用者名稱」、「客戶名稱」、* 「反向連結URL」和「IP位址」都會根據網站訪客和您的網路動態產生。

## 傳送歡迎電子郵件給使用者 {#section_kjp_c3s_p1b}

在使用者註冊帳戶後，您可以傳送歡迎電子郵件給使用者。 如果您設定驗證電子郵件，Studio會在傳送驗證電子郵件後傳送此電子郵件。 若要傳送歡迎電子郵件：

1. 在Studio中，按一下齒輪圖示以修改網路設定。
1. 按一下&#x200B;**[!UICONTROL Integration Settings > Livefyre Identity]**

1. 導覽至 **[!UICONTROL Email Settings]**。

1. 按一 **[!UICONTROL Send Welcome Emails To New Users]** 下以啟用傳送電子郵件。
1. 導覽至 **[!UICONTROL Network Email]** 設定「電子郵件 *標誌」、要用作寄件者地址(* Email From **)的電子郵件地址，以及用於寄件者電子郵件地址(電子郵件顯示名稱******)的顯示名稱。
