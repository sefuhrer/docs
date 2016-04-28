---

저작권:
  연도: 2015, 2016

---

# iOS 앱(Objective-C SDK)에서 Facebook 인증 사용
{: #facebook-auth-ios}

iOS 애플리케이션에서 Facebook을 ID 제공자로 사용하려면 Facebook 애플리케이션에 대한 iOS 플랫폼을 추가하고 구성하십시오. 

**팁:** Swift로 iOS 앱을 개발하는 경우 {{site.data.keyword.amashort}} 클라이언트 Swift SDK 사용을 고려하십시오. 이 페이지의 지시사항은 {{site.data.keyword.amashort}} 클라이언트 Objective-C SDK에 적용됩니다. Swift SDK 사용에 대한 지시사항은 [iOS 앱(Swift SDK)에서 Facebook 인증 사용](https://console.{DomainName}/docs/services/mobileaccess/facebook-auth-ios-swift-sdk.html)을 참조하십시오.

## 시작하기 전에
{: #facebook-auth-ios-before}
* {{site.data.keyword.amashort}}에서 보호하는 자원 및 {{site.data.keyword.amashort}} 클라이언트 SDK로 계측되는 iOS 프로젝트가 있어야 합니다. 자세한 정보는 [{{site.data.keyword.amashort}} 시작하기](https://console.{DomainName}/docs/services/mobileaccess/getting-started.html) 및 [iOS Objective-C SDK 설정](https://console.{DomainName}/docs/services/mobileaccess/getting-started-ios.html)을 참조하십시오.  
* {{site.data.keyword.amashort}} 서버 SDK로 백엔드 애플리케이션을 수동으로 보호하십시오. 자세한 정보는 [자원 보호](https://console.{DomainName}/docs/services/mobileaccess/protecting-resources.html)를 참조하십시오. 
* Facebook 애플리케이션 ID를 작성하십시오. 자세한 정보는 [Facebook 개발자 포털에서 Facebook 애플리케이션 ID 얻기](https://console.{DomainName}/docs/services/mobileaccess/facebook-auth-overview.html#facebook-appID)를 참조하십시오. 

## iOS 플랫폼에 대한 Facebook 애플리케이션 구성
{: #facebook-auth-ios-config}


1. Facebook 애플리케이션의 Facebook 개발자 포털에서 **설정 > 플랫폼 추가 > iOS**를 클릭하십시오. 

1. iOS 애플리케이션의 *번들 ID*를 지정하십시오. iOS 애플리케이션의 *번들 ID*를 찾으려면, `info.plist` 파일 또는 Xcode 프로젝트 **일반** 탭에서 **번들 ID**를 검색하십시오.
**팁**: 이러한 기능을 사용할 계획이라면 URL 스킴 접미부 또는 Single Sign On 사용을 고려하십시오. 

1. **설정 저장**을 클릭하십시오. 

## Facebook 인증을 사용하도록 {{site.data.keyword.amashort}} 구성
{: #facebook-auth-ios-configmca}

iOS 클라이언트를 제공하도록 Facebook 애플리케이션 ID 및 Facebook 애플리케이션을 구성한 후 {{site.data.keyword.amashort}}에서 Facebook 인증을 사용하도록 설정할 수 있습니다. 

1. {{site.data.keyword.Bluemix}} 대시보드에서 앱을 여십시오. 

1. **모바일 옵션**을 클릭하고 **라우트**(`applicationRoute`) 및 **앱 GUID**(`applicationGUID`)를 기록해 두십시오. SDK를 초기화하는 경우 이 값이 필요합니다. 

1. {{site.data.keyword.amashort}} 타일을 클릭하십시오. {{site.data.keyword.amashort}} 대시보드가 로드됩니다. 

1. **Facebook** 타일을 클릭하십시오.

1. Facebook 애플리케이션 ID를 지정하고 **저장**을 클릭하십시오. 

## iOS용 {{site.data.keyword.amashort}} 클라이언트 SDK 구성
{: #facebook-auth-ios-sdk}

### CocoaPods 설치
{: #facebook-auth-cocoapods}

{{site.data.keyword.amashort}} 클라이언트 SDK는 iOS 프로젝트에 대한 종속 항목 관리자인 CocoaPods를 사용하여 분배됩니다. CocoaPods는 저장소에서 아티팩트를 자동으로 다운로드하고 iOS 애플리케이션에서 아티팩트를 사용할 수 있게 합니다. 

1. 터미널을 열고 `pod --version` 명령을 실행하십시오. 이미 CocoaPods가 설치되어 있는 경우 버전 번호가 표시됩니다. 이 학습서의 다음 섹션으로 건너뛸 수 있습니다. 

1. `sudo gem install cocoapods`를 실행하여 CocoaPods를 설치하십시오. 추가적인 안내가 필요한 경우 [CocoaPods 웹 사이트](https://cocoapods.org/)를 참조하십시오. 

### CocoaPods로 {{site.data.keyword.amashort}} 클라이언트 SDK 설치
{: #facebook-auth-install-cocoapods}

1. iOS 프로젝트에서 `Podfile` 및 다음 행을 편집하십시오. 

	```
	pod 'IMFFacebookAuthentication'
	```

1. `Podfile`을 저장하고 명령행에서 `pod install` 명령을 실행하십시오. CocoaPods가 종속 항목을 설치합니다. 진행상태 및 추가된 컴포넌트가 표시됩니다.
**중요**: 이제 CocoaPods에서 생성한 `xcworkspace` 파일을 사용하여 프로젝트를 열어야 합니다. 일반적으로 이름은 `{your-project-name}.xcworkspace`입니다.   

1. iOS 프로젝트 작업공간을 열려면 명령행에서 `open {your-project-name}.xcworkspace`를 실행하십시오. 

### Facebook 인증을 사용하도록 iOS 프로젝트 구성
{: #facebook-auth-ios-configproject}

1. `info.plist` 파일을 찾으십시오. 이 파일은 보통 Xcode 프로젝트의 `지원 파일` 폴더에 있습니다. 

1. 다음 특성을 `info.plist` 파일에 추가하여 Facebook 통합을 구성하십시오. 

	![이미지](images/ios-facebook-infoplist-settings.png)

	Facebook 애플리케이션 ID를 사용하여 URL 스킴 및 FacebookappID 특성을 업데이트하십시오. 

또는 `info.plist` 파일을 마우스 오른쪽 단추로 클릭하고 **다른 이름으로 열기 > 소스 코드**를 선택한 후 다음 XML을 추가하여 파일을 업데이트할 수도 있습니다. 

 ```XML
	<key>CFBundleURLTypes</key>
	<array>
		<dict>
			<key>CFBundleURLSchemes</key>
			<array>
				<string>fb{your-facebook-application-id}</string>
			</array>
		</dict>
	</array>
	<key>FacebookAppID</key>
	<string>{your-facebook-application-id}</string>
	<key>FacebookDisplayName</key>
	<string>MyApp</string>
	<key>LSApplicationQueriesSchemes</key>
	<array>
		<string>fbauth</string>
		<string>fbauth2</string>
	</array>
	<key>NSAppTransportSecurity</key>
	<dict>
	    <key>NSExceptionDomains</key>
	    <dict>
	        <key>facebook.com</key>
	        <dict>
	            <key>NSIncludesSubdomains</key>
	            <true/>                
	            <key>NSThirdPartyExceptionRequiresForwardSecrecy</key>
	            <false/>
	        </dict>
	        <key>fbcdn.net</key>
	        <dict>
	            <key>NSIncludesSubdomains</key>
	            <true/>
	            <key>NSThirdPartyExceptionRequiresForwardSecrecy</key>
	            <false/>
	        </dict>
	        <key>akamaihd.net</key>
	        <dict>
	            <key>NSIncludesSubdomains</key>
	            <true/>
	            <key>NSThirdPartyExceptionRequiresForwardSecrecy</key>
	            <false/>
	        </dict>
	    </dict>
	</dict>
```
Facebook 애플리케이션 ID를 사용하여 URL 스킴 및 FacebookappID 특성을 업데이트하십시오.  **중요**: `info.plist` 파일의 기존 특성을 대체하고 있지 않는지 확인하십시오. 중첩된 특성이 있는 경우 수동으로 병합해야 합니다. 자세한 정보는 [Xcode 프로젝트 구성](https://developers.facebook.com/docs/ios/getting-started/) 및 [iOS9를 위한 앱 준비](https://developers.facebook.com/docs/ios/ios9)를 참조하십시오. 

## {{site.data.keyword.amashort}} 클라이언트 SDK 초기화
{: #facebook-auth-ios-initalize}

앱의 라우트(`applicationRoute`) 및 앱 GUID(`applicationGUID`)를 전달하여 클라이언트 SDK를 초기화하십시오.

필수는 아니지만 일반적으로 초기화 코드를 넣는 위치는 애플리케이션 위임자의 `application:didFinishLaunchingWithOptions` 메소드입니다. 

1. {{site.data.keyword.Bluemix_notm}} 대시보드의 기본 페이지를 열고 사용자 앱을 클릭하십시오. **모바일 옵션**을 클릭하고 **라우트**(`applicationRoute`) 및 **앱 GUID**(`applicationGUID`)를 기록해 두십시오.

1. 다음 헤더를 추가하여 {{site.data.keyword.amashort}} 클라이언트 SDK를 사용하려는 클래스에 필수 프레임워크를 가져오십시오. 

	**Objective-C**

	```Objective-C
	#import <IMFCore/IMFCore.h>
	#import <IMFFacebookAuthentication/IMFFacebookAuthenticationHandler.h>
	#import <FacebookSDK/FacebookSDK.h>
```

	**Swift**

	{{site.data.keyword.amashort}} 클라이언트 SDK는 Objective-C를 사용하여 구현되므로 Swift 프로젝트에 브리징 헤더를 추가해야 할 수 있습니다. 

	1. Xcode에서 마우스 오른쪽 단추로 프로젝트를 클릭하고 **새 파일...**을 선택하십시오. 
	* **iOS 소스** 카테고리에서 `헤더 파일`을 선택하십시오. 
	* `BridgingHeader.h`로 이름을 지정하십시오. 
	* 브리징 헤더에 아래 가져오기를 추가하십시오. 

	```Objective-C
	#import <IMFCore/IMFCore.h>
	#import <IMFFacebookAuthentication/IMFFacebookAuthenticationHandler.h>
	#import <FacebookSDK/FacebookSDK.h>
```
	* Xcode에서 프로젝트를 클릭하고 **빌드 설정** 탭을 선택하십시오. 
	* **Objective-C 브리징 헤더**를 검색하십시오. 
	* 값을 `BridgingHeader.h` 파일의 위치로 설정하십시오(예: `$(SRCROOT)/MyApp/BridgingHeader.h`). 
	* 프로젝트를 빌드하여 Xcode가 브리징 헤더를 선택 중인지 확인하십시오. 실패 메시지가 표시되지 않아야 합니다. 

3. 클라이언트 SDK를 초기화하십시오.	*applicationRoute* 및 *applicationGUID*를 {{site.data.keyword.Bluemix_notm}} 대시보드의 **모바일 옵션**에서 얻은 **라우트** 및 **앱 GUID** 값으로 바꾸십시오.

	**Objective-C**

	```Objective-C
	[[IMFClient sharedInstance]
			initializeWithBackendRoute:@"applicationRoute"
			backendGUID:@"applicationGUID"];
	```

	**Swift**

	```Swift
	IMFClient.sharedInstance().initializeWithBackendRoute("applicationRoute",
	 							backendGUID: "applicationGUID")
	```

1. Facebook SDK에 앱 활성화에 대한 알림을 전송하고 앱 위임자의 `application:didFinishLaunchingWithOptions` 메소드에 다음 코드를 추가하여 Facebook 인증 핸들러를 등록하십시오. IMFClient 인스턴스를 초기화한 후에 바로 이 코드를 추가하십시오. 

	**Objective-C**

	```Objective-C
		[FBAppEvents activateApp];
		[[IMFFacebookAuthenticationHandler sharedInstance] registerWithDefaultDelegate];
```

	**Swift**

	```Swift
		FBAppEvents.activateApp()
		IMFFacebookAuthenticationHandler.sharedInstance().registerWithDefaultDelegate()
```

1. 다음 코드를 앱 위임자에 추가하십시오. 

	**Objective-C**

	```Objective-C
	- (BOOL)application:(UIApplication *)application openURL:(NSURL *)url
			sourceApplication:(NSString *)sourceApplication annotation:(id)annotation {

		return [FBAppCall handleOpenURL:url sourceApplication:sourceApplication];


	}
```

	**Swift**

	```Swift
	func application(application: UIApplication, openURL url: NSURL,
					sourceApplication: String?, annotation: AnyObject) -> Bool {

		return FBAppCall.handleOpenURL(url, sourceApplication: sourceApplication)

	}
```

## 인증 테스트
{: #facebook-auth-ios-testing}
클라이언트 SDK가 초기화되고 Facebook 인증 관리자가 등록되면 모바일 백엔드에 대한 요청 작성을 시작할 수 있습니다. 

### 시작하기 전에
{: #facebook-auth-ios-testing-before}
{{site.data.keyword.mobilefirstbp}} 표준 유형을 사용해야 하며 이미 `/protected` 엔드포인트에 {{site.data.keyword.amashort}}에서 보호하는 자원이 있어야 합니다. `/protected` 엔드포인트를 설정해야 하는 경우
[자원 보호](https://console.{DomainName}/docs/services/mobileaccess/protecting-resources.html)를 참조하십시오. 

1. 브라우저에서 새로 작성된 모바일 백엔드의 보호 엔드포인트에 요청을 전송하십시오. URL `{applicationRoute}/protected`를 여십시오.
(예: `http://my-mobile-backend.mybluemix.net/protected`)
<br/>MobileFirst Services Starter 표준 유형으로 작성된 모바일 백엔드의 `/protected` 엔드포인트는 {{site.data.keyword.amashort}}를 사용하여 보호됩니다. 브라우저에 `Unauthorized` 메시지가 리턴됩니다. 이 엔드포인트는 {{site.data.keyword.amashort}} 클라이언트 SDK를 사용하여 계측되는 모바일 애플리케이션에서만 액세스할 수 있기 때문에 이 메시지가 리턴됩니다.

1. iOS 애플리케이션을 사용하여 동일한 엔드포인트에 대해 요청을 작성하십시오. 

	**Objective-C**

	```Objective-C
	NSString *requestPath = [NSString stringWithFormat:@"%@/protected",
								[[IMFClient sharedInstance] backendRoute]];

	IMFResourceRequest *request =  [IMFResourceRequest requestWithPath:requestPath
																method:@"GET"];

	[request sendWithCompletionHandler:^(IMFResponse *response, NSError *error) {
if (error){
			NSLog(@"Error :: %@", [error description]);
		} else {
			NSLog(@"Response :: %@", [response responseText]);
			NSLog("%@", IMFAuthorizationManager.sharedInstance().userIdentity)
		}
	}];
	```

	**Swift**

	```Swift
	let requestPath = IMFClient.sharedInstance().backendRoute + "/protected"

	let request = IMFResourceRequest(path: requestPath, method: "GET");
	request.sendWithCompletionHandler { (response, error) -> Void in
		if (nil != error){
			NSLog("Error :: %@", error.description)
		} else {
			NSLog("Response :: %@", response.responseText)
			NSLog("%@", IMFAuthorizationManager.sharedInstance().userIdentity)
		}
	};
 ```

1. 애플리케이션을 실행하십시오. Facebook 로그인 화면이 팝업으로 표시됩니다. 

	![이미지](images/ios-facebook-login.png)

	이 화면은 사용자 디바이스에 Facebook 앱이 설치되어 있지 않거나 현재 Facebook에 로그인되어 있지 않은 경우 약간 다르게 보일 수 있습니다. 

1. 인증을 위해 Facebook 사용자 ID를 사용할 수 있도록 {{site.data.keyword.amashort}}에 권한을 부여하려면 **확인**을 클릭하십시오. 

1. 	요청이 성공하면 Xcode 콘솔에 다음과 같은 출력이 표시됩니다.
	![이미지](images/ios-facebook-login-success.png)
