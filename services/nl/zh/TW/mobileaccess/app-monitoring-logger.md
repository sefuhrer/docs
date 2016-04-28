---

copyright:
  years: 2015, 2016
  
---

# 啟用、配置及使用日誌程式
{: #enable-logger}

{{site.data.keyword.amashort}} Client SDK 所提供的記載架構與您可能熟悉的其他日誌架構（例如 `java.util.logging` 或 `log4j`）類似。記載架構支援多個個別套件日誌程式實例、不同的記載層次、擷取應用程式當機的堆疊追蹤資料等。

您還可以將記載的資料配置為持續保存至本端儲存庫，然後可以根據需求將其傳送至 {{site.data.keyword.amashort}} 服務。

{{site.data.keyword.amashort}} Client SDK 記載架構支援下列記載層次（按詳細程度從低到高列出），建議的使用準則如下：

* `FATAL` - 用於無法復原的當機或停滯。FATAL 層次保留用於記載無法復原的錯誤，這些錯誤對於使用者會顯示為應用程式當機。
* `ERROR` - 用於非預期的異常狀況或非預期的網路通訊協定錯誤。
* `WARN` - 記載未視為重大錯誤的使用警告（例如使用已淘汰的 API 或網路回應緩慢）。
* `INFO` - 用於報告起始設定事件以及其他可能有用的資料。
* `DEBUG` - 用於報告除錯陳述，以協助開發人員解決應用程式問題報告。

請確定已在使用記載架構之前起始設定 {{site.data.keyword.amashort}} Client SDK。下列範例示範 {{site.data.keyword.amashort}} Client SDK 記載架構的基本用法。

### Android
{: #enable-logger-android}

```Java
BMSClient.getInstance().initialize(context, appRoute, appGUID);

Logger logger = Logger.getInstance("myLogger");

logger.debug("debug info");
logger.info("info message");
logger.warn("warning message");
logger.error("error message");
logger.fatal("fatal message");
```

### iOS - Objective-C
{: #enable-logger-objectc}

```Objective-C
[[IMFClient sharedInstance] initializeWithBackendRoute:appRoute backendGUID:appGUID];

IMFLogger *logger = [IMFLogger loggerForName:@"myLogger"];

[logger logDebugWithMessages:@"debug"];
[logger logInfoWithMessages:@"info"];
[logger logWarnWithMessages:@"warn"];
[logger logErrorWithMessages:@"error"];
[logger logFatalWithMessages:@"fatal"];

```

### iOS - Swift
{: #enable-logger-swift}

```Swift
IMFClient.sharedInstance().initializeWithBackendRoute(appRoute, backendGUID: appGuid)

let logger = IMFLogger(forName: "myLogger");

logger.logDebugWithMessages("debug");
logger.logInfoWithMessages("info");
logger.logWarnWithMessages("warn");
logger.logErrorWithMessages("error");
logger.logFatalWithMessages("fatal");
```

**附註：**{{site.data.keyword.amashort}} Client SDK 是使用 Objective-C 進行實作，因此您可能需要將 `IMFLoggerExtension.swift` 檔案新增至 Swift 專案，才能使用先前的日誌程式 API。您可以在 [Mobile Client Access Client SDK 保存檔](https://hub.jazz.net/git/bluemixmobilesdk/imf-ios-sdk/archive?revstr=master)中找到此檔案。


### Cordova
{: #enable-logger-android-cordova}

```JavaScript
BMSClient.initialize(appRoute , appGUID);

var logger = MFPLogger.getInstance("myLogger");

logger.debug("debug info");
logger.info("info message");
logger.warn("warning message");
logger.error("error message");
logger.fatal("fatal message");

```

您可以在 Logger 類別中找到下列其他方法：

* `setCapture` - 啟用或停用稍後要傳送至 {{site.data.keyword.amashort}} 服務之日誌資訊的持續保存。
* `setLevel` - 將最低記載層次設為儲存日誌訊息。
* `send` - 將持續保存的日誌傳送至 {{site.data.keyword.amashort}} 服務。

例如，當擷取為「開啟」狀態，並將日誌程式層次配置為 FATAL 時，日誌程式會擷取未捕捉的異常狀況。未捕捉的異常狀況通常對於使用者會顯示為應用程式當機，但並不會擷取任何導致當機事件的日誌。或者，更詳細的日誌程式層次可確保也會擷取導致 FATAL 日誌程式項目（例如 WARN 及 ERROR）的日誌。

**附註：**在 [SDK、範例、API 參考資料](sdks-samples-apis.html)中，尋找每一個平台的完整「日誌程式 API」參考資料。「日誌程式 API」是「{{site.data.keyword.amashort}} Client SDK 核心」的一部分。


## 範例用法
{: #sample-logger-usage}

下列程式碼 Snippet 顯示範例「日誌程式」用法：

### Android
{: #enable-logger-sample-android}

```Java
// Enable persisting logs
Logger.setCapture(true);

// Set the minimum log level to be printed and persisted
Logger.setLevel(Logger.LEVEL.INFO);

// Create two logger instances
Logger logger1 = Logger.getInstance("logger1");
Logger logger2 = Logger.getInstance("logger2");

// Log messages with different levels
logger1.debug("debug message");
logger2.info("info message");

// Send persisted logs to the {{site.data.keyword.amashort}} service
Logger.send();
```

### iOS - Objective-C
{: #enable-logger-sample-objectc}

```Objective-C
// Enable persisting logs
[IMFLogger setCapture:YES];

// Start capturing uncaught exceptions
[IMFLogger captureUncaughtExceptions];

// Set the minimum log level to be printed and persisted
[IMFLogger setLogLevel:IMFLogLevelInfo];

// Create two logger instances
IMFLogger *logger1 = [IMFLogger loggerForName:@"logger1"];
IMFLogger *logger2 = [IMFLogger loggerForName:@"logger2"];

// Log messages with different levels
[logger1 logDebugWithMessages:@"debug message"];
[logger2 logInfoWithMessages:@"info message"];

// Send persisted logs to the {{site.data.keyword.amashort}} service
[IMFLogger send];
```

### iOS - Swift
{: #enable-logger-sample-swift}

```Swift
// Enable persisting logs
IMFLogger.setCapture(true)

// Start capturing uncaught exceptions
IMFLogger.captureUncaughtExceptions()

// Set the minimum log level to be printed and persisted
IMFLogger.setLogLevel(IMFLogLevel.Info)

// Create two logger instances
let logger1 = IMFLogger(forName: "logger1");
let logger2 = IMFLogger(forName: "logger2");

// Log messages with different levels
logger1.logDebugWithMessages("debug message")
logger2.logInfoWithMessages("info message")

// Send persisted logs to the {{site.data.keyword.amashort}} service
IMFLogger.send()

```

### Cordova
{: #enable-logger-sample-cordova}

```JavaScript
// Enable persisting logs
MFPLogger.setCapture(true);

// Set the minimum log level to be printed and persisted
MFPLogger.setLevel(MFPLogger.INFO);

// Create two logger instances
var logger1 = MFPLogger.getInstance("logger1");
var logger2 = MFPLogger.getInstance("logger2");    

// Log messages with different levels
logger1.debug ("debug message");
logger2.info ("info message");

// Send persisted logs to the {{site.data.keyword.amashort}} service
MFPLogger.send(success, failure);
```

## 啟用 {{site.data.keyword.amashort}} Client SDK 內部日誌
{: #enable-logger-sdklogs}
目前只有 Android 版的 {{site.data.keyword.amashort}} Client SDK 才提供此特性。

{{site.data.keyword.amashort}} Client SDK 可提供較佳的開發體驗，原因是內部除錯訊息不會額外增加 Logcat 輸出。因此，預設不會列印由 {{site.data.keyword.amashort}} SDK 所產生且層次為 DEBUG 的內部日誌訊息。您可以使用下列 API，來啟用 {{site.data.keyword.amashort}} Client SDK 之所有內部日誌訊息的列印：


```
Logger.setSDKInternalLoggingEnabled(true);
```
