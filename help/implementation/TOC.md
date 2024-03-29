---
product: livefyre
audience: end-user
user-guide-title: Livefyre實施指南
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---


# Livefyre實施指南{#implementation}

+ [Livefyre實施指南](home.md)
+ 快速入門 {#getting-started}
   + [Livefyre整合快速入門](c-getting-started/c-getting-started.md)
   + 實施程序 {#implementation-process}
      + [實施程序](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [應用程式整合類型](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [應用程式實作](c-getting-started/designer-app-implementation.md)
      + [透過協力廠商整合實作Livefyre](c-app-integrations/implement-livefyre-3rd-party.md)
      + [架構](c-getting-started/c-implementation-process/c-architecture.md)
      + [內嵌應用程式](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [使用Livefyre.js將驗證新增至應用程式](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [建立伺服器端Token](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta Token](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [使用者驗證Token](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [使用CollectionMeta Token建立系列](t-create-a-collectionmeta-token.md)
      + [建立校驗和](c-creating-a-checksum.md)
+ 身分整合{#identity-integration}
   + [身分整合](t-about-identity-integration/t-about-identity-integration.md)
   + [驗證套件](t-about-identity-integration/c-authorization-package.md)
   + [AuthDelegate物件](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [將用戶權限發佈到外部系統（可選）](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + 實施SSO {#implementing-sso}
      + [實作SSO](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [除錯驗證委派](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + 與Livefyre {#sync-ping-for-pull}同步
      + [使用Ping for Pull與Livefyre同步](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [構建拉式端點](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [向Studio註冊端點](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [建立Ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [提取請求結構](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [建立Ping以取得回應](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Livefyre Identity {#livefyre-identity}
   + [Livefyre Identity](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [啟用Livefyre Identity](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + 搭配Livefyre身分識別使用社交應用程式{#use-social-apps-with-livefyre-identity}
      + [建立您的社交應用程式](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [建立Facebook應用程式以搭配Livefyre身分識別使用](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [建立Twitter應用程式以搭配Livefyre身分識別使用](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [建立Yahoo!與Livefyre Identity搭配使用的應用程式](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [建立Livefyre身分識別的LinkedIn應用程式](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [建立GitHub身分識別應用程式，以便與Livefyre身分識別搭配使用](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [使用Studio將您的社交應用程式連接至Livefyre實作](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [將Livefyre.js新增至頁面](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [初始化Livefyre身分](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [Livefyre身分識別電子郵件](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Janrain Capture/底板](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + 安裝 {#installation}
      + [安裝庫](c-installing-libraries/c-installing-libraries.md)
      + [類別和方法](c-installing-libraries/c-methods-livefyre.md)
      + [網路方法](c-installing-libraries/c-network-methods.md)
      + [setSSL網路方法](c-installing-libraries/r-setssl-method.md)
      + [buildLivefyreToken網路方法](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [buildUserAuthToken網路方法](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLivefyreToken網路方法](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncUrl網路方法](c-installing-libraries/r-setusersyncurl-method.md)
      + [syncUser Network Method](c-installing-libraries/r-syncuser-method.md)
      + [getUrn網路方法](c-installing-libraries/r-geturn-method.md)
      + [getUrnForUser Network方法](c-installing-libraries/r-geturnforuser-method.md)
      + [getNetworkName Network Method](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite網路方法](c-installing-libraries/r-getsite-method.md)
      + [網路類方法](c-installing-libraries/c-network-class-methods.md)
      + [系列類別方法](c-installing-libraries/c-collection-methods.md)
      + [createOrUpdate收集方法](c-installing-libraries/r-createorupdate-collection-method.md)
      + [buildCollectionMetaToken收集方法](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [buildChecksum收集方法](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent Collection方法](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [getUrn收集方法](c-installing-libraries/r-geturn-collection-method.md)
      + [網站類別方法](c-installing-libraries/c-site-methods.md)
      + [buildBlogCollection網站方法](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [buildChatCollection網站方法](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [buildCommentsCollection網站方法](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [buildCountingCollection網站方法](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [buildRatingsCollection網站方法](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [buildReviewsCollection網站方法](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [buildSitenotesCollection網站方法](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [buildCollection網站方法](c-installing-libraries/r-buildcollection-site-method.md)
      + [getUrn網站方法](c-installing-libraries/r-geturn-site-method.md)
      + [範例](c-installing-libraries/c-libraries-examples.md)
   + 行動 SDK {#mobile-sdks}
      + [行動 SDK](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [建立Livefyre Token C#](c-creating-livefyre-tokens-c-.md)
+ 應用程式整合{#app-integrations}
   + [聊天室](c-app-integrations/c-app-integratios-chat.md)
   + 意見 {#comments}
      + [意見](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [即時部落格](c-app-integrations/c-live-blog-integration.md)
   + [評論](c-app-integrations/c-reviews-integration.md)
   + Siestras {#sidenotes}
      + [Sides Integration](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [將字元號新增至頁面](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Sidesars應用程式事件](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [Sidesform配置選項](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [Sidesirs自訂樣式](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Siestroms自訂字串](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Sides Implementation](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [updateAnchors方法](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [地圖](c-app-integrations/c-map-integration.md)
   + [媒體牆](c-app-integrations/c-media-wall-integration.md)
   + [趨勢分析](c-app-integrations/c-trending-integration.md)
+ 應用程式自訂{#app-customizations}
   + [應用程式自訂](c-app-customizations/c-app-customizations.md)
   + [變更顯示選項](c-app-customizations/c-change-display-options.md)
   + [CSS類別](c-app-customizations/c-css-classes.md)
   + [Storify CSS類別](c-app-customizations/c-storify-css-classes.md)
   + [翻譯集](c-app-customizations/c-translation-sets.md)
   + [移動Livefyre標誌](c-app-customizations/c-move-the-livefyre-logo.md)
   + [限制媒體](c-app-customizations/c-restrict-media.md)
   + [隱藏應用程式元素](c-app-customizations/c-hide-app-elements.md)
   + [變更 @mention 圖示](c-app-customizations/c-change-mention-icon.md)
   + [反白顯示內容](c-app-customizations/c-highlight-content.md)
   + [自訂日期和時間戳記](c-app-customizations/c-date-time-stamp.md)
   + 功能內容{#feature-content}
      + [功能內容](c-app-customizations/t-feature-content.md)
      + [在Studio中啟用內容特色](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [從應用程式選取內容以加入功能](c-app-customizations/t-select-content-to-feature.md)
      + [從Studio選取要加入的內容](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [使用CSS來設定特色內容的樣式](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [功能API](c-app-customizations/c-feature-apis.md)
   + [使用AuthDelegate將Janrain連線至Livefyre](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [使用精選API匯總精選內容](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + 樣式內容{#style-content}
      + [使用者群組內容的樣式](c-app-customizations/c-style-user-group-content.md)
      + [新增使用者至群組](c-app-customizations/c-adding-users-to-groups.md)
   + 套用自訂樣式{#apply-custom-styles}
      + [套用自訂樣式](c-app-customizations/c-applying-custom-styles-.md)
      + [新增自訂按鈕](c-app-customizations/t-add-custom-buttons.md)
   + Javascript事件{#javascript-events}
      + [JavaScript事件定義與範例](c-app-customizations/c-javascript-events.md)
      + [視覺化應用程式的Javascript事件](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [媒體塗鴉牆的Javascript事件](c-app-customizations/c-javascript-events-media-wall.md)
      + [對話應用程式的Javascript事件](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [內嵌注釋應用程式](c-app-customizations/c-embed-a-comments-app.md)
   + [反向連結追蹤](c-app-customizations/c-referral-tracking.md)
   + [裝置與瀏覽器支援](c-app-customizations/c-device-and-browser-support.md)
   + [Twitter顯示需求](c-app-customizations/c-twitter-display-requirements.md)
+ [壓力測試政策](c-stress-test-policy.md)
+ Analytics {#analytics}
   + [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [搭配Adobe Analytics和動態標籤管理器(DTM)使用Livefyre](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [搭配使用Livefyre和其他Analytics工具](livefyre-analytics/c-livefyre-analytics.md)
   + [Livefyre Analytics事件](livefyre-analytics/c-livefyre-analytics-events.md)
+ [整合Livefyre與AEM](c-livefyre-aem-integration.md)
+ 進階主題{#advanced-topics}
   + [顯示注釋計數](c-advanced-topics/t-display-comment-count.md)
   + [啟用社交共用](c-advanced-topics/c-enabling-social-sharing.md)
   + [活動串流](c-advanced-topics/c-activity-stream.md)
   + [引導HTML](c-advanced-topics/c-bootstrap-html.md)
   + [變更系列](c-advanced-topics/c-change-collection.md)
   + [多個系列](c-advanced-topics/c-multiple-collections.md)
   + [切換核心應用程式類型](c-advanced-topics/c-switch-core-app-types.md)
   + [社交計數器](c-advanced-topics/c-social-counter.md)
   + [搭配Livefyre應用程式使用Bootsrap和Stream API](c-advanced-topics/bootstrap-stream-api.md)
