---
product: livefyre
audience: 使用者
user-guide-title: Experience Manager Livefyre實作指南
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Experience Manager Livefyre實作指南 {#implementation}

+ [Livefyre實施指南](home.md)
+ [Livefyre整合快速入門](c-getting-started/c-getting-started.md)
   + 實施 {#implementation-process}
      + [實作程序](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [應用程式整合類型](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [應用程式建置](c-getting-started/designer-app-implementation.md)
      + [使用協力廠商整合實施Livefyre](c-app-integrations/implement-livefyre-3rd-party.md)
      + [架構](c-getting-started/c-implementation-process/c-architecture.md)
      + [內嵌應用程式](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [使用Livefyre. js新增驗證至應用程式](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [建置伺服器端Token](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta Token](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [使用者驗證Token](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [使用CollectionMeta Token建立系列](t-create-a-collectionmeta-token.md)
      + [建立檢查加總](c-creating-a-checksum.md)
+ 身分整合
   + [身分整合](t-about-identity-integration/t-about-identity-integration.md)
   + [驗證套件](t-about-identity-integration/c-authorization-package.md)
   + [authDelegate物件](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [將使用者權限張貼至外部系統(可選)](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + 實作SSO {#implementing-sso}
      + [實作SSO](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [除錯Auth委派](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + 與Livefyre同步 {#sync-ping-for-pull}
      + [與Livefyre同步，以用於提取](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [建立提取端點](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [使用Studio註冊端點](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [建立Ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [提取請求結構](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [建立用於提取回應的Ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Livefyre身份識別 {#livefyre-identity}
   + [Livefyre身份識別](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [啓用Livefyre身分識別](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + 使用Livefyre身分識別搭配使用社交應用程式
      + [建立您的社交應用程式](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [建立Facebook應用程式以搭配Livefyre身分識別](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [建立Google Project以搭配Livefyre身分識別](c-livefyre-identity-comp/t-create-a-google-project-for-use-with-livefyre-identity.md)
      + [建立Twitter應用程式以搭配Livefyre身分識別](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [建立Yahoo！應用程式搭配Livefyre身分識別](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [建立Microsoft Live Identity App以搭配Livefyre身分識別使用](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [建立LinkedIn應用程式以搭配Livefyre身分識別使用](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [建立GitHub身分應用程式以搭配Livefyre身分識別使用](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [使用Studio將您的社交應用程式連接到您的Livefyre實作](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [將Livefyre. js新增至頁面](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [初始化Livefyre身分識別](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [Livefyre身分識別的電子郵件](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Janrain Capture/Backflight](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + 安裝 {#installation}
      + [安裝資料庫](c-installing-libraries/c-installing-libraries.md)
      + [類別與方法](c-installing-libraries/c-methods-livefyre.md)
      + [網路方法](c-installing-libraries/c-network-methods.md)
      + [setSSL網路方法](c-installing-libraries/r-setssl-method.md)
      + [BuildLiveLifeToken網路方法](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [BuilduserAuthToken網路方法](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLiveRetoken網路方法](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncURL網路方法](c-installing-libraries/r-setusersyncurl-method.md)
      + [SyncUser Network方法](c-installing-libraries/r-syncuser-method.md)
      + [Geturn Network方法](c-installing-libraries/r-geturn-method.md)
      + [getEnfor使用者網路方法](c-installing-libraries/r-geturnforuser-method.md)
      + [getPrevikName網路方法](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite Network方法](c-installing-libraries/r-getsite-method.md)
      + [網路類別方法](c-installing-libraries/c-network-class-methods.md)
      + [系列類別方法](c-installing-libraries/c-collection-methods.md)
      + [CreateOrdUpdate Collection方法](c-installing-libraries/r-createorupdate-collection-method.md)
      + [BuildCollectionMetaoken Collection方法](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [BuildCheckSum Collection方法](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent Collection方法](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [Geturn Collection方法](c-installing-libraries/r-geturn-collection-method.md)
      + [網站類別方法](c-installing-libraries/c-site-methods.md)
      + [BuildSocialCollection網站方法](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [BuildchatCollection網站方法](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [buildCommentScollection網站方法](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [BuildIdentijectCollection網站方法](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [BuildratingScollection網站方法](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [BuildDreviewScollection網站方法](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [BuildSitenoteCollection網站方法](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [BuildCollection網站方法](c-installing-libraries/r-buildcollection-site-method.md)
      + [Geturn網站方法](c-installing-libraries/r-geturn-site-method.md)
      + [範例](c-installing-libraries/c-libraries-examples.md)
   + 行動SDK {#mobile-sdks}
      + [行動SDK](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre. js](c-livefyre.js.md)
+ [建立Livefyre Tokens C#](c-creating-livefyre-tokens-c-.md)
+ 應用程式整合 {#app-integrations}
   + [聊天室](c-app-integrations/c-app-integratios-chat.md)
   + 注釋 {#comments}
      + [注釋](c-app-integrations/c-comments-integration/c-comments-integration.md)
      + [注釋中的廣告](c-app-integrations/c-comments-integration/c-ads-in-comments-integration.md)
   + [即時部落格](c-app-integrations/c-live-blog-integration.md)
   + [評論](c-app-integrations/c-reviews-integration.md)
   + Sitents {#sidenotes}
      + [Sitdones整合](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [將Sitdenes新增至頁面](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Sitdones應用程式事件](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [Sites設定設定選項](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [Sitdenes自訂樣式](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Sitdones自訂字串](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Sitdones實施](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
   + [地圖](c-app-integrations/c-map-integration.md)
   + [Media Wall](c-app-integrations/c-media-wall-integration.md)
   + [趨勢分析](c-app-integrations/c-trending-integration.md)
+ 應用程式自訂 {#app-customtizations}
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
   + 功能內容
      + [功能內容](c-app-customizations/t-feature-content.md)
      + [在Studio中啓用內容](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [從應用程式選取內容至功能](c-app-customizations/t-select-content-to-feature.md)
      + [從Studio選取內容功能](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [使用CSS至樣式特色內容](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [功能API](c-app-customizations/c-feature-apis.md)
   + [使用AuthDelegate將Janrain與Livefyre連結](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [使用精選API匯總精選內容](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + 樣式內容
      + [樣式使用者群組內容](c-app-customizations/c-style-user-group-content.md)
      + [新增使用者至群組](c-app-customizations/c-adding-users-to-groups.md)
   + 套用自訂樣式
      + [套用自訂樣式](c-app-customizations/c-applying-custom-styles-.md)
      + [新增自訂按鈕](c-app-customizations/t-add-custom-buttons.md)
   + Javascript事件
      + [JavaScript事件定義和範例](c-app-customizations/c-javascript-events.md)
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
   + [使用Livefyre搭配Adobe Analytics和Dynamic Tag Manager(DTM)](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [搭配其他Analytics工具使用Livefyre](livefyre-analytics/c-livefyre-analytics.md)
   + [Livefyre Analytics Events](livefyre-analytics/c-livefyre-analytics-events.md)
+ [將Livefyre與AEM整合](c-livefyre-aem-integration.md)
+ 進階主題 {#advanced-topics}
   + [顯示註解計數](c-advanced-topics/t-display-comment-count.md)
   + [啓用社交共用功能](c-advanced-topics/c-enabling-social-sharing.md)
   + [活動資料流](c-advanced-topics/c-activity-stream.md)
   + [啓動載入HTML](c-advanced-topics/c-bootstrap-html.md)
   + [變更系列](c-advanced-topics/c-change-collection.md)
   + [多個系列](c-advanced-topics/c-multiple-collections.md)
   + [切換核心應用程式類型](c-advanced-topics/c-switch-core-app-types.md)
   + [社交計數器](c-advanced-topics/c-social-counter.md)
   + [搭配使用Bootsrap和Stream API與Livefyre應用程式](c-advanced-topics/bootstrap-stream-api.md)