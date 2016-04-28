---



copyright:

  years: 2015, 2016



---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# {{site.data.keyword.Bluemix_notm}} Local および {{site.data.keyword.Bluemix_notm}} Dedicated の管理
{: #mng}
*最終更新日: 2016 年 2 月 18 日*

{{site.data.keyword.Bluemix_notm}} Local または {{site.data.keyword.Bluemix_notm}} Dedicated の管理者権限がある場合は、**「管理」**ページに移動して、リソースの管理、割り当て量の使用状況のモニター、ユーザー許可の管理、アップグレード通知のスケジュール設定、セキュリティー・レポートおよびログの表示などを行います。組織の管理は、スペースを作成し、ユーザーの役割と権限を設定することによって行うことができます。『[組織の管理](../admin/adminpublic.html#orgmng)』を参照してください。
{:shortdesc}

*表 1. {{site.data.keyword.Bluemix_notm}} Local または Dedicated のインスタンスを管理するための管理用タスク*

| 選択可能な操作 | 詳細 |    
|----------------|---------|
|システム使用状況のモニター | **「管理」&gt;「使用量」**をクリックします。システム情報を表示し、CPU 使用量をモニターし、使用量の計画を立てて、ビジネスにとって最良の決定を行ってください。『[使用量情報の表示](index.html#oc_resource)』を参照してください。|
|カタログの管理 | どのサービスをユーザーおよび組織が表示できるようにするかを管理するには、**「管理」&gt;「カタログ管理」**をクリックします。『[カタログの管理](index.html#oc_catalog)』を参照してください。|
|組織の管理 | 組織を作成し、組織の割り当て量をモニターし、ニーズに沿った決定を素早く行うには、**「管理」&gt;「組織管理」**をクリックします。『[組織の管理](index.html#oc_organizations)』を参照してください。|
|スペースの作成とユーザーの役割の割り当て | 組織内のスペースを作成するには、**「アカウントとサポート」**アイコン ![アカウントとサポート](../support/images/account_support.svg) をクリックして、**「組織の管理」**を選択します。ユーザーを追加し、組織およびスペースの役割をユーザーに割り当てます。『[組織の管理](../admin/adminpublic.html#orgmng)』を参照してください。 |
|管理ユーザーの権限の管理 | ユーザーの追加、ユーザーの削除、およびユーザーの許可の調整を行うには、**「管理」&gt;「ユーザー管理」**をクリックします。『[ユーザーおよび許可の管理](index.html#oc_user)』を参照してください。 |
|レポートおよびログのレビュー | ユーザーのインスタンスのセキュリティー・レポートおよび監査ログを表示するには、**「管理」&gt;「レポートおよびログ」**をクリックします。『[レポートの表示](index.html#oc_report)』を参照してください。 |
|システム情報の表示 | 保留中の更新、インスタンスの名前とバージョン、地域、API URL、CLI URL、LDAP 構成の詳細、グループとユーザーのマッピング、統計、および共有ドメインなどのシステム情報を表示するには、**「管理」&gt;「システム情報」**をクリックします。「保留中の更新」セクションでは、通知を拡張するためにカレンダー・フィードおよびイベント・サブスクリプションにアクセスすることもできます。『[システム情報の表示](index.html#oc_system)』を参照してください。 |
|通知の拡張およびイベント・サブスクリプションのセットアップ | **「管理」&gt;「システム情報」&gt;「*Number* 件の更新が保留中」**をクリックします。Web フックを使用して、選択した Web サービスと統合し、更新またはインシデントに関するイベント通知サブスクリプションをセットアップできます。『[通知およびイベント・サブスクリプション](index.html#oc_eventsubscription)』を参照してください。 |


## 通知およびイベント・サブスクリプション
{: #oc_eventsubscription}

「状況」ページを確認することによって、常にご使用の環境の状況を把握できます。また、{{site.data.keyword.Bluemix_notm}} は、定期保守やアップグレードなどのイベントに関する通知を「管理」ページの「通知」エリアに送信します。インシデントは「状況」ページに報告されます。

### 通知

お客様はローカル環境または専用環境について IBM からの通知を表示し、環境の状況をモニターすることができます。次の表で、各種のタイプの通知および通知が表示される場所に関する情報を確認してください。

| **イベント・タイプ** | **通知方法** |       
|-----------------|-------------------|
| 保守の更新情報 | 近く予定されている保守の更新に関するアラートは「管理」ページの「通知」で受け取ります。**「管理」**ページに移動して、**「通知」**アイコン ![通知](images/icon_announcement.svg) を選択します。保留中および完了した通知の全リストおよび履歴を確認するには、**「管理」&gt;「システム情報」** &gt;「*Number* 件の**更新が保留中 **」をクリックします。イベント・サブスクリプションをセットアップして、通知機能を拡張できます。例えば、「管理」ページからの保守更新アラートを、選択した Web サービスと統合して、メッセージをヘルプ・デスクの E メール・アドレスに経路指定したり、SMS メッセージを、選択した電話番号に経路指定したりするようセットアップできます。 |
| 重大なインシデント | 重大なインシデントに関するアラートは「状況」ページで受け取ります。**「アカウントとサポート」**アイコン ![アカウントとサポート](../support/images/account_support.svg) をクリックして、**「状況」**を選択します。イベント・サブスクリプションをセットアップして、通知機能を拡張できます。例えば、「状況」ページからのインシデント・アラートを、選択した Web サービスと統合して、メッセージをヘルプ・デスクの E メール・アドレスに経路指定したり、SMS メッセージを、選択した電話番号に経路指定したりするようセットアップできます。 |  
| 状況 | プラットフォーム、サービス、および {{site.data.keyword.Bluemix_notm}} インスタンスの最新状況を表示できます。**「アカウントとサポート」**アイコン ![アカウントとサポート](../support/images/account_support.svg) をクリックして、**「状況」**を選択します。  |

*表 2. イベント・タイプと通知方法*

### イベント・サブスクリプションのセットアップ

Web フックを実装したイベント・サブスクリプションを使用することにより、「管理」ページおよび「状況」ページに送信される通知の機能を拡張できます。Web フックは、ヘルプ・デスクの E メール・アドレス (E メールで) や電話番号 (SMS メッセージで) など、選択した宛先に直接、通知を経路指定します。通知のタイプ (具体的には、保守更新アラートまたは重大なインシデント・アラート) および通知に含める情報をカスタマイズできます。

Web フックを使用して特定のイベント・サブスクリプションをセットアップするには、以下の手順を実行します。

1. **「管理」**ページに移動して、以下を行います。

- 保守更新の通知の場合は、**「システム情報」** &gt;「*Number* 件の**更新が保留中**」に移動して、**「サブスクライブ」**アイコン ![サブスクライブ](images/icon_subscribe.svg) をクリックします。
- インシデント・アラートの通知の場合は、**「アカウントとサポート」**アイコン ![アカウントとサポート](../support/images/account_support.svg) &gt; **「状況」**をクリックし、次に**「サブスクライブ」**アイコン ![サブスクライブ](images/icon_subscribe.svg) をクリックします。

**注**: 説明されている 2 つの方法のいずれかを使用して、両方のタイプの通知のイベント・サブスクリプション・ページにアクセスできます。

2. **「サブスクリプションの追加」**をクリックします。

3. イベント・サブスクリプション・フォームに記入します。フォームの各フィールドについては、次の表を確認してください。

| **フィールド** | **説明** |
|-----------------|-------------------|
| タイプ  | Web フックを選択します。 |
|  方法  | GET または POST を選択します。 |
| イベント | 更新またはインシデントに関する通知にサブスクライブすることを選択します。 |
| URL | Web サービスにフックする URL を入力します。 |
| 説明 | 作成するイベント・サブスクリプションの説明を追加します。 |
| ユーザ名 | Web サービスのユーザー名を入力します。個人の資格情報を使用したくない場合は、{{site.data.keyword.Bluemix_notm}} 専用に使用する機能 ID をセットアップできます。 |
| パスワード | Web サービスのパスワードを入力します。 |
| ペイロード | POST 方式を選択した場合は、使用する Web サービスに固有のプロパティーを、IBM 通知に使用される値とペアにして入力します。例えば、Web サービスからの通知にタイトル、メッセージ、および重大度を表示する場合は、{{site.data.keyword.Bluemix_notm}} の値を Web サービスの一致するプロパティーと組み合わせて定義する必要があります。通知タイトル、メッセージ本文、および重大度レベルに関する情報を {{site.data.keyword.Bluemix_notm}} 通知から引き出す場合は、`"{{title}}`、`"{{message}}、"`、および `"{{severity}}"` の値を使用できます。このセクションに情報を入力しないと、追加情報が何もない通知を受け取ります。  |

表 3. イベント・サブスクリプション・フォームのフィールド

イベント・サブスクリプションを保存すると、Web サービスを介してセットアップした方式を使用して通知を受け取ります。通知は、従来どおり、インシデントの場合は「状況」ページ、保守更新の場合は「管理」ページの「通知」エリアに表示されます。

保存されたイベント・サブスクリプションを選択して、最新のアクティビティーを表示することができます。最新のアクティビティー項目をクリックして展開すると、詳細を表示できます。詳細には、ペイロード・セクションに使用できる、通知に関する IBM の値が含まれています。これらの値を確認するには、最新のアクティビティー項目を展開し、**「イベント」**を展開し、次に**「オブジェクト」**を展開します。


## システム情報の表示
{: #oc_system}

システム情報を表示するには、**「管理」&gt;「システム情報 (SYSTEM INFORMATION)」** をクリックします。

保留中の更新、全般的なシステム情報、および LDAP 構成の詳細に関する様々なセクションを展開して表示することができます。

### 保留中の更新と通知

「更新」セクションでは、お客様の側でのアクションが必要な保留中の更新の通知数を確認できます。特定の更新に対してアクションを起こすには、以下のステップを実行します。


<ol>
<li><strong>「<em>Number</em> 件の更新が保留中 (Number updates pending)」</strong>をクリックして、保留中の更新をすべて表示します。</li>
<li>アクションを起こすべき更新を選択するか、または更新の詳細 (更新期間、スケジュール日、中断状況など) を表示します。</li>
<li><strong>「利用不能日の設定 (SET UNAVAILABLE DATES)」</strong>をクリックして、更新期間の内、更新の適用には不適当な特定の日を設定します。利用不能日を設定すると、IBM はお客様の選択内容に基づいて更新を承認し、スケジュールに入れます。更新が承認されてスケジュールに入ると、通知が届きます。</li>
<li>利用不能日がなければ、<strong>承認 (APPROVE)</strong>をクリックして更新を承認します。承認すると、スケジュールに入っている更新期間中に更新が適用されます。IBM からは、更新のデプロイメントの開始時と終了時に通知が送信されます。</li>
</ol>

**注**: お客様が利用不能日を設定せず、更新も承認しない場合、プラットフォームが現行の最新状態で維持されるように、更新が 21 日の期間の最後に適用されます。

「保留中の更新」ページから、更新スケジュールの追跡を行うことを選択できます。これを行うには、**「カレンダー」**アイコン ![カレンダー](images/icon_calendar.svg) をクリックして、`.ics` ファイルをダウンロードし、スケジュールに入っている更新を、選択したカレンダー・アプリにインポートします。

<ol>
<li>カレンダー・アプリを開きます。</li>
<li>**「カレンダー」**アイコン ![カレンダー](images/icon_calendar.svg) をクリックしてカレンダー・ファイルをダウンロードし、`.ics` ファイルを使用してカレンダー・ファイルをカレンダー・アプリにインポートします。</li>
<li>資格情報を入力します。</li>
<li>スケジュールに入っている更新を表示します。</li>
</ol>

また、イベント・サブスクリプションを使用して、選択した Web サービスと統合することにより、「管理」ページの通知機能を拡張することもできます。更新またはインシデントに関するイベント通知サブスクリプションをセットアップするには、『[イベント・サブスクリプションと通知](index.html#oc_eventsubscription)』を参照してください。

### 一般的なシステム情報

「一般情報 (General Information)」セクションでは、以下の情報を表示できます。

- {{site.data.keyword.Bluemix_notm}} ビルドに関する基本情報。
- バージョン、URL、地域、および CLI 資料へのリンクが含まれた API 情報。
- システムおよびサービスに関する共有ドメイン情報。
- アプリケーション、ユーザー、および組織の総数に関する統計。

### LDAP 構成の詳細

「LDAP 構成の詳細 (LDAP Configuration Details)」セクションでは、LDAP サーバーを選択し、ユーザーとグループのマッピング情報を表示できます。{{site.data.keyword.IBM}} WebID を使用している場合は、このセクションに示されます。

## 使用量情報の表示
{: #oc_resource}

ローカル・インスタンスまたは専用インスタンスおよび {{site.data.keyword.Bluemix_notm}} アカウントに関するさまざまなタイプの使用量情報を表示できます。

- リソース情報 (ディスク・スペース、CPU 使用量、ネットワーク使用量、および平均応答時間を含む)。『[リソース使用量](index.html#resourceusage)』を参照してください。
- 組織ごとのアカウント使用 (ランタイム・アプリ数と使用量、ランタイム GB 時間の合計数、およびサービス・インスタンス数と使用量を含む)。『[アカウント使用量](index.html#accountusage)』を参照してください。
- 組織のメモリー割り当て量の使用量、合計使用済みメモリー割り当て量に基づいて割り振られたアプリ・メモリー、および特定の組織のアプリごとの GB 時間使用量の表示。また、「組織管理」ページの「割り当て量のモニター」セクションに、すべての組織の割り当て量の使用状況を表示することもできます。『[組織管理](../admin/index.html#orgusage)』を参照してください。


### リソース使用量
{: #resourceusage}

リソース情報を表示するには、**「管理」&gt;「使用量」**をクリックします。

「リソース・モニタリング (Resource Monitoring)」セクションでは、以下の情報を表示できます。

- リソース使用率情報 (何 GB のメモリー、何 GB のディスク・スペースが使用されているか、など)。すべての Droplet Execution Agent  (DEA) での平均 CPU 使用量を表示することができます。**「CPU」**タイルをクリックすることで、各 DEA の CPU 使用量を表示できます。使用量が最も大きい DEA が先頭にリストされます。各 DEA は、ジョブと IP アドレスによって識別されます。CPU 使用量は、システム・プロセスで使用された CPU 量、ユーザー・プロセスで使用された CPU 量、および待機プロセスで使用された CPU 量の 3 つのカテゴリーに分かれています。
- 入力帯域幅および出力帯域幅のネットワーク使用率情報 (過去 1 日、1 週間、または 1 カ月)。
表示されるデータは、パブリック・ネットワークとプライベート・ネットワークの両方の入出力トラフィックの合計に基づいています。
- {{site.data.keyword.Bluemix_notm}} の平均応答時間 (過去 10 分、1 時間、および 1 日)。
- {{site.data.keyword.Bluemix_notm}} の 1 秒あたりの平均トランザクション数 (過去 10 分、1 時間、および 1 日)。

### アカウント使用量
{: #accountusage}

専用環境またはローカル環境のアカウントの月々の使用量を表示できます。このデータを使用して、使用量に基づいて特定の組織に対する課金額を特定できます。

<ol>
<li><strong>「アカウントとサポート」</strong>アイコン ![アカウントとサポート](../support/images/account_support.svg) &gt; <strong>「アカウント」</strong> &gt; <strong>「使用量詳細」</strong>をクリックします。</li>
<li>データを表示する組織を選択します。</li>
<li>以下のカテゴリーの使用量詳細を表示できます。<ul>
<li>使用量のあるランタイム・アプリ</li>
<li>ランタイム・アプリの合計使用量 (GB 時間)</li>
<li>使用量のあるサービス・インスタンス</li>
</ul>
</li>
<li>オプション: <strong>「クラウド・アクティビティー」</strong>メニューを使用して、月を選択し、特定の月のデータを表示します。</li>
<li>オプション: <strong>「データのエクスポート」</strong>をクリックして、<strong>CSV</strong> または <strong>JSON</strong> を選択し、選択した月のデータを <code>CSV</code> ファイルまたは <code>JSON</code> ファイルにエクスポートします。</li>
</ol>

{{site.data.keyword.Bluemix_notm}} Public からシンジケートされるランタイム、アプリ、およびサービスについて、月々の使用量および関連する料金をアカウント・レベルで表示することもできます。このデータを使用して、使用量に基づいて特定の組織に対する課金額を特定できます。

<ol>
<li><strong>「アカウントとサポート」</strong>アイコン ![アカウントとサポート](../support/images/account_support.svg) &gt; <strong>「アカウント」</strong> &gt; <strong>「使用量詳細」</strong>をクリックします。</li>
<li><strong>「パブリック」</strong>をクリックします。</li>
<li>データを表示する組織を選択するか、あるいは、すべての組織のデータを一度に表示するために<strong>「すべての組織」</strong>を選択します。</li>
<li>以下のカテゴリーの使用量詳細を表示できます。<ul>
<li>使用量のあるランタイム・アプリ</li>
<li>ランタイム・アプリの合計使用量 (GB 時間)</li>
<li>使用量のあるサービス・インスタンス</li>
<li>シンジケートされたすべてのランタイム、サービス、およびアプリの課金の要約</li>
</ul>
</li>
<li>オプション: 棒グラフから月を選択して、特定の月のデータを表示します。デフォルトでは、今月のデータが表示されます。</li>
<li>オプション: <strong>「データのエクスポート」</strong>をクリックして、<strong>CSV</strong> または <strong>JSON</strong> を選択し、選択した月のデータを <code>CSV</code> ファイルまたは <code>JSON</code> ファイルにエクスポートします。</li>
</ol>


### 組織の使用量
{: #orgusage}

組織ごとの使用量を表示するには、**「管理」&gt;「組織管理」**をクリックし、**「組織リスト」**から組織を選択します。選択した組織の**「組織の管理」**ページに、以下の使用量情報を表示できます。

- 現在使用中のサービスの数。
- 現在使用中の経路の数。
- 割り当て量のうち、どのくらいの量が現在使用されており、どのくらいの量が現在使用されていないかを示す、メモリー割り当て量グラフ。
- どのアプリケーションが使用済みメモリー割り当て量に含まれているかを示す、アプリケーション割り振りグラフ。
- デプロイされたアプリごとの 3 カ月間の使用 GB 時間数のレポートを表示する、従量制アプリケーション使用量グラフ。**「リスト表示」**を選択すると、すべてのアプリについて、アプリごとのメモリー割り振りおよび過去 3 カ月間の従量制 GB 時間使用量などのデータを確認できます。

組織ごとの使用量の表示、割り当て量プランの調整、および組織の管理について詳しくは、『[組織の管理](../admin/index.html#oc_organizations)』を参照してください。

## レポートの表示
{: #oc_report}

ご使用の {{site.data.keyword.Bluemix_notm}} インスタンスに関して、セキュリティー・レポートやログ (DataPower&trade;、ファイアウォール、およびログイン監査など) を表示できます。

レポートやログを表示するには、**「管理」&gt;「レポートおよびログ (REPORTS AND LOGS)」**をクリックします。

以下のオプションから選択します。

- フィールドから開始日および終了日を選択して、表示するレポートとログをフィルタリングできます。

- ナビゲーション・ペインから各種レポートを展開および表示できます。
- レポートおよびログのコレクション内で検索できます。検索は、レポート名に加え、レポートおよびログ内に含まれているテキスト・コンテンツにも適用されます。**「管理イベント (Administration Events)」**、**「DataPower レポート (DataPower Reports)」**、**「ファイアウォール (Firewall)」**、および**「ログイン監査 (Login Audit)」**によって検索をフィルターに掛けることもできます。
- レポートまたはログを表示している時、![ダウンロード](images/icon_download.png) アイコンをクリックするとレポートをダウンロードできます。

以下の表では、{{site.data.keyword.Bluemix_notm}} Local および {{site.data.keyword.Bluemix_notm}} Dedicated 用に生成されるセキュリティー・レポートのリストを示します。

| **カテゴリー** | **レポート** | **説明** |      
|-----------------|-------------------|---------------------|
| ファイアウォール | ファイアウォールのログイン | Vyatta ファイアウォール・デバイスへの管理者のログインに関するイベント。 |
| ファイアウォール | ファイアウォールの拒否 | 設定されているファイアウォール・ルールに従ってアクセス要求が拒否された場合に Vyatta ファイアウォール・デバイスによって生成されるイベント。 |
| {{site.data.keyword.Bluemix_notm}} 管理者のログイン・イベント | {{site.data.keyword.Bluemix_notm}} 管理者のログイン | 管理者が各 {{site.data.keyword.Bluemix_notm}} システム上で SSH セッションを開始したときにオペレーティング・システムによって生成されるイベント。 |
| {{site.data.keyword.Bluemix_notm}} アプリケーション開発者のログイン・イベント | {{site.data.keyword.Bluemix_notm}} アプリケーション開発者のログイン | コマンド・ライン、REST API、または {{site.data.keyword.Bluemix_notm}} ユーザー・インターフェースを使用して {{site.data.keyword.Bluemix_notm}} プラットフォーム・ユーザーがセッションを開始したときに {{site.data.keyword.Bluemix_notm}} プラットフォーム・ログイン・コンポーネントによって生成されるイベント。 |
| {{site.data.keyword.Bluemix_notm}} 管理者の管理イベント | {{site.data.keyword.Bluemix_notm}} 管理者のオペレーティング・システム管理イベント | 管理者が現行作業セッション内でアクションを実行したときにオペレーティング・システムによって生成されるイベント。 |
| {{site.data.keyword.Bluemix_notm}} アプリケーション開発者の管理イベント | {{site.data.keyword.Bluemix_notm}} (Cloud Foundry) 管理イベント | コマンド・ライン、REST API、または {{site.data.keyword.Bluemix_notm}} ユーザー・インターフェースを使用して {{site.data.keyword.Bluemix_notm}} プラットフォーム・ユーザーによって実行された操作に関連するイベント。 |
| {{site.data.keyword.Bluemix_notm}} 管理者のデータベース管理イベント | データベース管理イベント | {{site.data.keyword.Bluemix_notm}} 内部データベースでデータベース管理者によって実行された操作に関連するイベント。 |
| 管理イベント | ユーザー管理イベント | 「管理」ページで実行されたユーザー管理アクションに関連するイベント。 |
| 管理イベント | catalog | サービス・カタログの変換に関連するイベント。 |
| 管理イベント | セキュリティー・レポート管理イベント | 「管理」ページで実行されたセキュリティー・レポート管理アクションに関連するイベント。 |
| アクセス・レビュー | アクセス・レビュー・レポート | 特権アクセスのレビュー。 |
| 変更管理 | ソフトウェア変更管理 | 変更管理アクティビティー。 |
| 鍵管理 | カスタム SSL 証明書の管理 | アップロードおよび保管されたカスタム SSL 証明書。 |
| 暗号化 | 転送中のデータ暗号化 | 構成されている転送中のデータ暗号化。 |
| アンチウィルス | アンチウィルス・スキャン・レポート | 配置されているアンチウィルス・ソフトウェア。 |
| ソフトウェア・フィックス管理 | パッチ適用レポート | 適用されたソフトウェア・フィックス。 |
| セキュリティー・インシデント管理 | セキュリティー・インシデント修復レポート | セキュリティー・インシデント管理のセキュリティー・インシデントのエビデンス。 |

*表 4. セキュリティー・レポートのリスト*

## 状況の表示
{: #oc_status}

{{site.data.keyword.Bluemix_notm}} インスタンスの状況は、{{site.data.keyword.Bluemix_notm}} の「状況」ページを使用してモニターできます。**「アカウントとサポート」**アイコン ![アカウントとサポート](../support/images/account_support.svg) をクリックして、**「状況」**を選択します。

「状況」ページは、{{site.data.keyword.Bluemix_notm}} プラットフォームや {{site.data.keyword.Bluemix_notm}} 内の主要なサービスに影響を及ぼす重要な事象に関する通知や発表を見つけるための中心的な場所です。

通知を調べずに済むように、通知の RSS フィードをサブスクライブすることができます。「状況」ページおよび RSS フィードのセットアップについて詳しくは、『[{{site.data.keyword.Bluemix_notm}} の表示](../support/index.html#viewing-bluemix-status)』を参照してください。

## カタログの管理
{: #oc_catalog}

{{site.data.keyword.Bluemix_notm}} カタログで、どの {{site.data.keyword.Bluemix_notm}} サービスおよびスターターをユーザーに表示するかを管理することができます。**「管理」&gt;「カタログ管理」**をクリックします。

サービスまたはスターターのタイルを選択して、サービスまたはスターターのプランの表示可能性を編集します。表示可能性を編集するには、以下のオプションから選択します。

- 非表示のサービスまたはスターターを表示して、「カタログ」でユーザーに表示されるようにするには、**「すべてのプランを有効化 (ENABLE ALL PLANS)」**を選択します。
- {{site.data.keyword.Bluemix_notm}} カタログで、サービスやスターターをユーザーに対して非表示にするには、**「すべてのプランを無効化 (DISABLE ALL PLANS)」**を選択します。
- 個別プランの表示可能性を制御するには、プラン名を選択してから、ドロップダウン・メニューを使用して**「すべての組織に対して有効化 (Enable for all organizations)」**、 **「すべての組織に対して無効化 (Disable for all organizations)」**、または**「特定の組織に対してプランを有効化 (Enable plan for specific organizations)」**を選択します。

<!-- staging only start -->

### サービス・ブローカーの登録
{: #servicebrokerui}

{{site.data.keyword.Bluemix_notm}} カタログに表示するサービスがある場合、サービス・ブローカーを実装して登録する必要があります。ブローカーを登録した後、ローカル・インスタンスまたは専用インスタンス内のサービスにアクセス可能な組織を選択できます。

サービス・ブローカーを処理する方法は、サービス・ブローカーが管理するサービスの数や、サービス・ブローカーが既に {{site.data.keyword.Bluemix_notm}} に登録されているかどうかによって異なります。

- サービス・ブローカーが 1 つのサービスを管理する場合、[Service Broker API](http://docs.cloudfoundry.org/services/api.html){: new_window} の実装後に、ユーザー・インターフェースを使用してサービス・ブローカーを登録できます。 『[1 つのサービスを管理するサービス・ブローカーの登録](index.html#registerbrokerui)』を参照してください。
- サービス・ブローカーが複数のサービスを管理する場合、現時点では、Service Broker API の実装後にサービス・ブローカーを登録することはできません。代わりに、[{{site.data.keyword.Bluemix_notm}} 管理 CLI](../cli/plugins/bluemix_admin/index.html) プラグイン (`ba` サブコマンド) で cf CLI を使用するか、[カスタム・サービス API](index.html#servicebrokerapi) を使用します。
- サービス・ブローカーが既に登録されていて、それを更新または削除する場合、[{{site.data.keyword.Bluemix_notm}} 管理 CLI](../cli/plugins/bluemix_admin/index.html) プラグイン (`ba` サブコマンド) で cf CLI を使用するか、[カスタム・サービス API](index.html#servicebrokerapi) を使用します。

#### 1 つのサーバーを管理するサービス・ブローカーの登録
{: #registerbrokerui}

サービス・ブローカーを登録するには、以下の手順を実行します。

1\. [Cloud Foundry Service Broker API を実装](http://docs.cloudfoundry.org/services/api.html){: new_window}し、サービスと {{site.data.keyword.Bluemix_notm}} との間の通信を可能にします。Service Broker API は、{{site.data.keyword.Bluemix_notm}} が利用する REST エンドポイントのセットです。

サービス・ブローカーを実装する際に、`GET /v2/catalog` の JSON 応答で、サービスの定義とサービス・プラン (表示するサービス情報を含む) を指定する必要があります。例として、以下のカタログ (GET) 応答のサンプル JSON を検討してください。

```
"services":[
{
      "bindable":true,
      "description":"Cool Service is a data warehousing and analytics solution.",
      "id":"cool-service-id",
      "name":"coolservice",
      "tags":[
         "customer_dedicated"
      ],
      "metadata":{
         "displayName":"Cool Service",
         "serviceMonitorApi":"https://myservicesstatus.mybluemix.net/healthcheck/",
         "providerDisplayName":"Cool company",
         "longDescription":"Cool Service is a data warehousing and analytics solution. You can quickly move your data into a next-generation columnar in-memory database and start running complex analytical queries.",
         "bullets":[
            {
               "title":"Fast and Simple",
               "description":"Cool Service uses dynamic in-memory columnar technology and innovations, such as parallel vector processing and actionable compression to rapidly scan and return relevant data."
            },
            {
               "title":"Connectivity",
               "description":"Cool Service is built to let you connect easily and to all of your services and applications. You can start analyzing your data right away with familiar tools."
            }
         ],
         "featuredImageUrl":"http://path/to/icon_64x64.png",
         "imageUrl":"http://path/to/icon_50x50.png",
         "mediumImageUrl":"http://path/to/icon_32x32.png",
         "smallImageUrl":"http://path/to/icon_24x24.png",
         "documentationUrl":"http://path/to/documentation.html",
         "instructionsUrl":"http://path/to/servicesample.md",
         "termsUrl":"http://path/to/terms_of_agreement.pdf",
         "media":[
            {
               "type":"youtube",
               "thumbnailUrl":"http://path/to/thumbnail.png",
               "url":"http://path/to/youtube/video",
               "caption":"Using Cool Service in 60 Seconds"
            },
            {
               "type":"image",
               "thumbnailUrl":"http://path/to/thumbnail.png",
               "url":"http://path/to/image_file.png",
               "caption":"Cool Service connects applications"
            },
            {
               "type":"video",
               "thumbnailUrl":"http://path/to/thumb.png",
               "caption":"Cool Service works with tables",
               "source":[
                  {
                     "type":"video/mp4",
                     "url":"http://path/to/video_file.mp4"
                  },
                  {
                     "type":"video/ogg",
                     "url":"http://path/to/video_file.ogg"
                  }
               ]
            }
         ]
      },
      "plans":[
         {
            "name":"smallplan",
            "description":"Dedicated schema and tablespace per service instance on a shared server. 1GB and 10GB of compressed database storage can hold up to 5GB and 50GB of uncompressed data respectively based on typical compression ratios.",
            "free":false,
            "id":"cool-service-plan-id",
            "metadata":{
               "bullets":[
                  "1 GB Min per instance. 10 GB Max per instance."
               ],
               "costs":[
                  {
                     "unitId":"INSTANCES_PER_MONTH",
                     "unit":"MONTHLY",
                     "partNumber":"D15UTLL"
                  }
               ],
               "displayName":"Small"
            }
         }
      ]
   }
]
}
```
{: codeblock}

**注**: ローカル環境または専用環境のサービス・ブローカーを作成する場合、サービス定義 JSON ファイルの 「tags」フィールドに `customer_dedicated` を指定する必要があります。

2\. Service Broker API の実装後、**「管理」&gt;「カタログ管理」**に移動します。

3\. **「サービス・ブローカーの登録」**をクリックします。

4\. 以下のフィールドに値を入力して、フォームを完成させます。

- サービス・ブローカー名
- サービス・ブローカー URL
- サービス・ブローカー・ユーザー名
- サービス・ブローカー・パスワード

5\. **「接続」**をクリックします。

6\. 利用可能なプラン、アイコン、およびサービスの説明など、サービスの情報を確認します。

**注**: サービスのカタログ情報を変更する必要がある場合は、サービス・ブローカーを更新し、フォームに記入して、再度、登録プロセスを開始します。

7\. **「登録」**をクリックします。

8\. サービスのすべてのプランを有効にするか、特定のプランのみを有効にするかを選択します。デフォルトでは、すべてのプランが無効になっています。

9\. すべての組織または特定の組織のサービス・インスタンスを有効にします。

これで、サービスが {{site.data.keyword.Bluemix_notm}} カタログの「カスタム・サービス」カテゴリーに表示されるようになりました。**「管理」&gt;「カタログ管理」**に移動し、カタログでタイルを選択します。いつでも、別のプランを有効にしたり、組織に対するプランの表示可能性を編集したりできます。

## 組織の管理
{: #oc_organizations}

組織の作成と削除、組織の管理者の追加または削除、および割り当て量の使用状況のモニターを行って組織を管理し、ビジネスにとって最良の決定を下すことができます。

**「管理」&gt;「組織管理 (ORGANIZATION ADMINISTRATION)」**をクリックします。

さまざまなセクションを展開および表示できます。組織の割り当て量プランを確認および管理することもできます。

### 組織の作成

新規の組織を作成し、管理者を追加するには、以下の手順を実行します。

1. <strong>「組織の作成」</strong>をクリックします。
2. 組織の名前を入力します。
3. 管理者として追加する個人の名前または E メールを入力します。複数の名前を入力および選択することで、複数のマネージャーを追加できます。
4. <strong>「組織の作成」</strong>をクリックし、変更を保存して組織を作成します。

### 割り当て量のモニター

「割り当て量のモニター (Quota Monitoring)」セクションでは、セクションを展開して、以下の情報を表示できます。

- 環境メモリー使用量。このセクションでは、完全なシステム環境のメモリー使用量が詳細に示されます。
グラフで、使用中システム・メモリー、合計システム・メモリー、使用済みの割り当て量、および割り振られている合計割り当て量を含む情報が示されます。以下の用語リストで、グラフに表示されるメモリー使用量のタイプを定義します。

	<dl>
	<dt><strong>使用中システム・メモリー (Used system memory)</strong></dt>
	<dd>環境で使用されている物理メモリー。</dd>
	<dt><strong>合計システム・メモリー (Total system memory)</strong></dt>
	<dd>環境で使用可能な合計物理メモリー。</dd>
	<dt><strong>デプロイ済み割り当て量 (Quota deployed)</strong></dt>
	<dd>すべての組織でデプロイされているすべてのアプリ用に割り振られているメモリーの合計。デプロイ済み割り当て量の合計は、環境の物理的な合計システム・メモリーを超過する可能性があります。例えば、合計システム・メモリーが 16 GB で、合計 5 個の異なる組織にそれぞれ 4 GB のメモリーを割り振った場合、合計割り当て量は、すべての組織についてお客様に割り振られている合計システム・メモリーを超過しています。ただし、多くの場合、各組織に個別に割り振られている合計割り当て量を各組織が使用していないことが考えられます。また、すべての組織が、それぞれに割り振られている合計メモリー割り当て量を同時に使用しないことが考えられます。</dd>
	<dt><strong>合計割り当て量 (Total quota)</strong></dt>
	<dd>すべての組織に割り振られている合計メモリー。</dd>
	</dl>

- 組織のメモリー使用量。このセクションでは、組織レベルでのメモリー使用量の詳細が示されます。合計割り当て量、および各組織にデプロイされている割り当て量を表示できます。グラフで、組織別の最も大きいメモリー使用量をリストした情報が示されます。デフォルトでは、使用メモリー量が最大の組織がリストの先頭になります。**「最大メモリー使用量 (Highest Memory Usage)」**および**「過剰メモリー割り振り (Excess Memory Allocation)」**を基準としてソートできます。

	<dl>
	<dt><strong>最大メモリー使用量 (Highest Memory Usage)</strong></dt>
	<dd>このオプションは、最大メモリー量を使用している組織を特定するために使用します。使用メモリー量が最も多い組織を特定するため、最大メモリー使用量を基準としてソートします。リストは、デプロイ済み割り当て量によってソートされます。</dd>
	<dt><strong>過剰メモリー割り振り (Excess Memory Allocation)</strong></dt>
	<dd>このオプションは、必要より大きい割り当て量プランが設定されている組織を識別する場合に使用します。
	過剰メモリー使用量を基準としてソートすることで、当該組織に割り振られている割り当て量に対して使用メモリー量が最小の組織を識別します。</dd>
	</dl>

### 割り当て量プランの調整

組織の割り当て量プランを変更するには、以下の手順を実行します。

<ol>
<li>「組織のメモリー使用量」セクションで、グラフ内で編集する組織のバーをクリックするか、「組織リスト」セクションで組織の名前を選択します。</li>
<li>「組織の管理」ページでは、割り当て量プランの変更、組織の名前の変更、およびマネージャーの追加/削除を行うことができます。<br />
<p><strong>注</strong>: 組織の現在の使用量には不十分な割り当てプランを選択した場合、メッセージを受け取ります。</p>
</li>
<li>「組織の管理」ページで行った変更を保存するには、<strong>「保存」</strong>をクリックします。</li>
</ol>

### 組織リストからの組織の管理

「組織リスト」セクションでは、{{site.data.keyword.Bluemix_notm}} 環境内のすべての組織を表示することができ、組織名をクリックして個別の組織に対するアクションを実行できます。

- 組織を削除するには、「アクション」列の**「削除」**アイコン ![削除](images/icon_trash.svg) をクリックします。
- 組織の割り当て量プランおよび割り当て量の使用状況を表示するには、リスト内の組織の名前をクリックします。選択した組織の**「組織の管理」**ページで、以下の使用量情報を表示できます。

  - 現在使用中のサービスの数。
  - 現在使用中の経路の数。
  - 割り当て量のうち、どのくらいの量が現在使用されており、どのくらいの量が現在使用されていないかを示す、メモリー割り当て量グラフ。
  - どのアプリケーションが使用済みメモリー割り当て量に含まれているかを示す、アプリケーション割り振りグラフ。
  - デプロイされたアプリごとの 3 カ月間の使用 GB 時間数のレポートを表示する、従量制アプリケーション使用量グラフ。**「リスト表示」**を選択すると、すべてのアプリについて、アプリごとのメモリー割り振りおよび過去 3 カ月間の従量制 GB 時間使用量などのデータを確認できます。

- 組織の名前の編集や、管理者の追加または削除を行うには、リスト内の組織の名前をクリックし、画面のプロンプトに従います。

## ユーザーおよび許可の管理
{: #oc_useradmin}

LDAP を使用し、自社のユーザー・レジストリーからご使用の {{site.data.keyword.Bluemix_notm}} インスタンスにユーザーを追加できます。ユーザーは、個別またはグループで追加できます。また、ユーザー許可を表示できます。`admin` 許可が割り当てられている場合、他のユーザーの許可を設定および管理することもできます。**「管理」&gt;「ユーザー管理 (USER ADMINISTRATION)」**をクリックします。

「ユーザー管理 (User Administration)」ページに、ローカル・インスタンスまたは専用インスタンスのユーザーが全員表示されます。
各ユーザーの許可が表示されます。許可は、None、`Admin`、`Catalog`、`Login`、`Reports`、および `Users` のいずれかになります。許可を有効にするか、または目的の許可について `view` 権限または `write` アクセス権限をユーザーに与えることができます。許可および権限はアイコンで示されます。アイコンの各タイプと説明については、『[許可](#permissions)』を参照してください。

以下のオプションから選択します。

* ユーザーを検索します。**「検索」**フィールドを使用して、表内のユーザーを検索できます。
* ユーザーを追加します。`admin` 許可、または `write` アクセス権限がある `users` 許可を持っている場合、ユーザーを追加することができます。ユーザーまたはユーザーのグループを追加するには、**「単一ユーザーの追加 (ADD SINGLE USER)」**または**「ユーザー・グループの追加 (ADD USER GROUP)」**をクリックします。**「検索」**フィールドに、検索対象のユーザー名またはグループ名を入力し、**「組織 (Org)」**リストからユーザーまたはユーザー・グループの追加先となる組織を選択します。追加するユーザーまたはグループが見つかったら、ユーザー名をクリックしてから、**「単一ユーザーの追加 (ADD USER)」**または**「複数ユーザーの追加 (ADD USERS)」**をクリックして追加します。50 人を超えるユーザーのグループは、バックグラウンド・バッチ・ジョブを介して追加されます。追加操作が成功すると、ユーザーまたはグループが表に追加され、表示および検索できるようになります。追加されたユーザーには、許可は割り当てられていません。
* 許可および組織を編集します。`admin` 許可を持っている場合、他のユーザーの許可および組織を編集することができます。許可を編集するには、ユーザーを特定し、ユーザー名をクリックします。許可を有効または無効にするには、開いたウィンドウに含まれている、以下のオプションから選択します。
	* 許可を有効にするには、リストから**「オン (On)」**を選択します。
	* リストから**「読み取り」**を選択して、ユーザーにその許可について `view` (読み取り専用) アクセス権限を持たせるか、**「書き込み」**を選択して、その許可について `write` (編集、追加、削除) アクセス権限を持たせます。
	* 許可を無効にするには、**「オフ (Off)」**を選択します。組織を編集するには、以下のオプションから選択します。
	* 検索フィールドを使用して組織を特定し、クリックしてオプションから選択し、**「追加」**をクリックして、ユーザーを組織に追加します。
	* ![削除。負符号で示されている](images/icon_remove.svg) アイコンをクリックして、組織からユーザーを削除します。終了したら、**「保存」**をクリックします。
* ユーザーを削除します。`admin` 許可、または `write` アクセス権限がある `users` 許可を持っている場合、ユーザーを削除することができます。ユーザーを削除するには、そのユーザーを検索し、![「削除」](images/icon_trash.svg)アイコンをクリックし、次に**「削除」**をクリックします。

### 許可
{: #permissions}

ユーザーには、以下の許可を割り当てることができます。

| **ユーザー許可** | **説明** |       
|-----------------|-------------------|
| admin | `admin` 許可を備えているユーザーは、他のユーザーの許可を編集できます。 |
| catalog | `catalog` 許可を持つユーザーには、ローカル・インスタンスまたは専用インスタンスで利用できるサービスを `view` または `write` (modify) するアクセス権限を割り当てることができます。 |  
| login | `login` 権限を持つユーザーは、「管理」ページを表示できます。この権限がない場合、ユーザーは「管理」メニュー・オプションを表示できません。 |
| reports | `reports` 許可を持つユーザーには、セキュリティー・レポートを `view` または `write` (modify) するアクセス権限を割り当てることができます。 |
| users | `users` 許可を持つユーザーには、ユーザー・リストを `view` するアクセス権限、またはユーザーを `write` (add または remove) するアクセス権限を割り当てることができます。この許可では、他のユーザーの許可を設定することはできません。|

*表 5. 許可*

許可を有効にするか、または目的の許可について `view` アクセス権限または `write` アクセス権限をユーザーに与えることができます。許可および権限は次のアイコンで示されます。

* ![有効。チェック・マークで示されている](images/icon_enabled.svg) アイコン (許可の横) は、その許可が有効になっていることを示しています。
* ![表示。目で示されている](images/icon_read.svg) アイコンは、そのユーザーに、その許可について `view` (read-only) アクセス権限があることを示しています。

* ![書き込み。鉛筆で示されている](images/icon_write.svg) アイコンは、そのユーザーに、その許可について `write` (edit、add、remove) アクセス権限があることを示しています。


## Admin REST API を使用したユーザーの管理
{: #usingadminapi}

`Admin` REST API を使用して、{{site.data.keyword.Bluemix_notm}} インスタンスのユーザーの追加と削除を行うことができます。`Admin` REST API のエンドポイントおよび JSON のリソースは、コマンド・ラインからの基本操作を可能にするために実験に基づいて提供されています。この情報の例に含まれているエンドポイントと URL は、急な通知で変更または廃止される可能性があります。

以下のツールは、この後の例を使用するための前提条件です。他のツールを使用するという選択肢もあります。

* cURL。REST API 要求をコマンドとして入力するために必要です。cURL は、HTTP 要求をサーバーに送信し、コマンド・ライン・インターフェースを介してサーバー応答を受信するための、無料ユーティリティーです。cURL は、[cURL Download サイト](http://curl.haxx.se/download.html){: new_window}からダウンロードできます。
* Python。Python の pretty-print JSON ツールを使用するために必要です。このオプション・ツールは、JSON テキストを入力として取り、読みやすい出力を提供します。Python は、[Python Downloads サイト](https://www.python.org/downloads){: new_window}からダウンロードできます。

### 管理コンソールへのログイン

`Admin` API 要求を実行する前に、管理コンソールにログインする必要があります。`admin` 許可、または `write` アクセス権限のある `users` 許可を持っている場合、ユーザーを追加または削除することができます。他のユーザーの許可を編集するには、`admin` 許可を持っている必要があります。

管理コンソールにログインするには、`https://<your_host>.ibm.com/login` エンドポイントで基本アクセス認証を使用できます。サーバーは、セッションで Cookie を返します。その Cookie を、管理コンソールのすべての操作に使用します。

**注:** 数時間使用されない場合、そのセッションは無効になります。

管理コンソールにログインするには、次のコマンドを実行します。

`curl --user <user_id>:<password> -c ./cookies.txt --header "Accept: application/json" https://<your_host>.ibm.com/login | python -m json.tool`
{: codeblock}

<dl class="parml">

<dt class="pt dlterm">--user <em>user_id</em>:<em>password</em></dt>
<dd class="pd">ユーザー ID とパスワードを受け入れ、Basic 許可ヘッダーを送信します。</dd>


<dt class="pt dlterm">-c <em>filename</em></dt>
<dd class="pd">指定されたユーザー ID とパスワードを、指定されたファイルに Cookie として保管します。</dd>


<dt class="pt dlterm">--header</dt>
<dd class="pd">Accept ヘッダーを送信します。</dd>

</dl>

このコマンドの出力例を以下に示します。
```
{
    "message": "Logged in",
    "name": {
        "familyName": "*last_name*",
        "givenName": "*first_name*"
    }
}
```
{: screen}

### 組織のリスト表示
{: #listingorg}

ユーザーを追加する場合は、組織を指定する必要があります。`Admin` REST API を使用して、すべての組織をリストすることができます。組織をリストするには、`read` アクセス権限のある `users` 許可を持っている必要があります。組織をすべてリストするには、以下のコマンドを実行します。

`curl -b ./cookies.txt https://<your_host>.ibm.com/codi/v1/organizations | python -m json.tool`
{: codeblock}

<dl class="parml">

<dt class="pt dlterm">-b <em>filename</em></dt>
<dd class="pd"><samp class="ph codeph">-c</samp> オプションを使用してあらかじめファイルに保管されていたユーザー ID とパスワードを、Cookie として HTTP サーバーに渡します。</dd>

</dl>

各組織について、結果には次の情報が含まれます。
* `"guid"`、組織の GUID
* `"name"`、組織の名前

このコマンドの出力例を以下に示します。
```
{
     "resources": [
         {
             "guid": "05af098d-d476-4fb0-8b87-a84350e72af3",
             "name": "org-1"
         },
         {
             "guid": "5129a5a8-37c2-4ee4-a9b2-bebae3531db5",
             "name": "org-2"
         },

		 		 ....

		 ],
		 "total_results": 284
}
```
{: screen}

### ユーザーのリスト表示
{: #listingusr}

`Admin` REST API を使用して、登録済みのユーザーをリストすることで、目的のユーザーが既に {{site.data.keyword.Bluemix_notm}} 環境に追加されているかどうかを確認できます。
登録済みのユーザーをリストするには、`read` アクセス権限のある `users` 許可を持っている必要があります。ユーザーを全員リストするには、以下のコマンドを実行します。

`curl -b ./cookies.txt https://<your_host>.ibm.com/codi/v1/users | python -m json.tool`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-b <em>filename</em></dt>
<dd class="pd"><samp class="ph codeph">-c</samp> オプションを使用してあらかじめファイルに保管されていたユーザー ID とパスワードを、Cookie として HTTP サーバーに渡します。</dd>
</dl>

登録されている各ユーザーについて、結果には次の情報が含まれます。
* `"first_name"` (名) と `"last_name"` (姓)
* `"user_id"`、ユーザー ID と E メール・アドレス
* `"guid"`、組織の GUID。
* `"permissions"`、管理コンソールのユーザーに割り当てられる。

このコマンドの出力例を以下に示します。


```
{
    "next_url": "/codi/v1/users?results_per_page=100&amp;page=2",
    "prev_url": "",
    "resources": [
        {
            "active": true,
            "created_at": "2015-04-08T17:38:51.788Z",
            "created_by": "",
            "first_name": "some first name",
            "guid": "5d5268cf-39c0-48d3-96ae-7afe928e5dd7",
            "last_name": "some last name",
            "permissions": [
                {
                    "display": "ops.admin"
},
                {
                    "display": "ops.catalog.write"
},
                {
                    "display": "ops.reports.write"
},
                {
                    "display": "ops.catalog.read"
},
                {
                    "display": "ops.users.write"
},
                {
                    "display": "ops.reports.read"
},
                {
                    "display": "ops.login"
},
                {
                    "display": "ops.users.read"
                }
            ],
            "user_id": "someid@us.ibm.com"
        },
		 		 ...


     }
    ],
    "total_pages": 395,
    "total_results": 39421
}

```
{: screen}

### ユーザーの追加

`Admin` REST API を使用して、{{site.data.keyword.Bluemix_notm}} インスタンスにユーザーを追加できます。ユーザーを追加するには、`write` アクセス権限のある `users` 許可を持っている必要があります。

追加するユーザーは 1 人だけでもかまわないし、ユーザーのリストを追加することもできます。ユーザーを 1 つの組織に追加することも、複数の組織に追加することもできます。ユーザーを追加するには、以下の情報を指定する必要があります。

* ユーザーのファーストネーム (名) とラストネーム (姓)。「[ユーザーのリスト表示](index.html#listingusr)」にある、`"first_name"` と `"last_name"` を指定します。
* E メール・アドレスとユーザー ID。E メール・アドレスとユーザー ID についてはどちらも、「[ユーザーのリスト表示](index.html#listingusr)」にある `"user_id"` を指定します。
* `"guid"`。「[組織のリスト表示](index.html#listingorg)」にある組織の GUID を指定します。

情報は、JSON ファイルで提供します。

`curl -b ./cookies.txt https://<your_host>.ibm.com/codi/v1/users | python -m json.tool`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-b <em>filename</em></dt>
<dd class="pd"><samp class="ph codeph">-c</samp> オプションを使用してあらかじめファイルに保管されていたユーザー ID とパスワードを、Cookie として HTTP サーバーに渡します。</dd>
</dl>

<ol>
<li>適切な JSON 形式で情報を含む JSON ファイルを作成します。<p>例えば、以下の内容を含む、`user.json` という名前のファイルを作成します。
</p>
<pre>
{
    "members": [
        {
            "emails": [
"some_user_id@domain.com"
],
            "first_name": "Some_first_name",
            "last_name": "Some_last_name",
            "user_id": "some_user_id@domain.com"
        }
    ],
    "organization_roles": [
        {
            "id": "7a891f9c-e4e7-46c7-8b4e-dffaa7eb3bcd"
        }
    ]
}
</pre>
</li>
<li>以下のコマンドを実行して、JSON ファイルのコンテンツをユーザーのエンドポイントに投稿します:<br/><br/>
<code>
curl -v -b ./cookies.txt -X POST -H "Content-Type: application/json" -d @./user.json https://<your_host>.ibm.com/codi/v1/users
</code>
</li>
</ol>

<dl class="parml">

<dt class="pt dlterm">-v </dt>
<dd class="pd">詳細出力を指定します。</dd>


<dt class="pt dlterm">-X POST</dt>
<dd class="pd">デフォルトの GET 要求をオーバーライドして、POST 要求を指定します。</dd>


<dt class="pt dlterm">-H "Content-Type: application/json"</dt>
<dd class="pd">content-type ヘッダーを指定します。この場合、JSON です。</dd>


<dt class="pt dlterm">-d *data*</dt>
<dd class="pd">POST 要求で HTTP サーバーに送信するデータ (この場合、ファイル `user.json`) を指定します。</dd>

</dl>



このコマンドの出力例を以下に示します。


```
* Connected to localhost (127.0.0.1) port 3000 (#0)
 
 > POST /codi/v1/users HTTP/1.1
 > User-Agent: curl/7.37.1
 > Host: localhost:3000
 > Accept: */*
 > Cookie: opsConsole.sid=s%3AHLcwKGumyEb3IxREmikDOG3ATKD5xYMe.jfjWAa1tJC0rGghpeV8RPHqE2JaFVL4ZFIJbQpSC%2FAI
 > Content-Type: application/json
 > Content-Length: 333
 >
 * upload completely sent off: 333 out of 333 bytes
 < HTTP/1.1 201 Created
 < x-powered-by: Express
 < vary: X-HTTP-Method-Override
 < content-type: application/json
 < date: Wed, 22 Apr 2015 19:32:54 GMT
 < connection: close
 < transfer-encoding: chunked
 < X-Time_Check: Proxy Time: 5612 msec
 ```
{: screen}

### ユーザーの削除

`Admin` REST API を使用して、{{site.data.keyword.Bluemix_notm}} インスタンスからユーザーを削除できます。ユーザーを削除するには、`write` アクセス権限のある `users` 許可を持っている必要があります。

ユーザーを削除するには、そのユーザーのユーザー ID を指定する必要があります。次のコマンドを実行します。

`curl -v -b ./cookies.txt -X DELETE https://<your_host>.ibm.com/codi/v1/users?user_id=<some_user_id@domain.com>`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-X DELETE</dt>
<dd class="pd">DELETE 要求を指定します。</dd>
</dl>

このコマンドの出力例を以下に示します。


```
 * connect to ::1 port 3000 failed: Connection refused
 *   Trying 127.0.0.1...
 * Connected to localhost (127.0.0.1) port 3000 (#0)
 
 > DELETE /codi/v1/users?user_id=exampleuser@domain.com HTTP/1.1
 > User-Agent: curl/7.37.1
 > Host: localhost:3000
 > Accept: */*
 > Cookie: opsConsole.sid=s%3AHLcwKGumyEb3IxREmikDOG3ATKD5xYMe.jfjWAa1tJC0rGghpeV8RPHqE2JaFVL4ZFIJbQpSC%2FAI
 >
 < HTTP/1.1 201 Created
 < x-powered-by: Express
 < content-type: application/json
 < date: Wed, 22 Apr 2015 21:01:09 GMT
 < connection: close
 < transfer-encoding: chunked
 < X-Time_Check: Proxy Time: 1922 msec
 <
 ```
{: screen}


## カスタム・サービス API
{: #servicebrokerapi}

新規サービスの登録または作成、サービスの更新、およびサービスの削除に使用できる 3 つの API があります。

すべての API は、<code>https://console.&lt;subdomain&gt;.bluemix.net/</code> に対して相対的になります。

<dl>
<dt><strong>&lt;subdomain&gt;</strong></dt>
<dd>この値は、ローカル・インスタンスまたは専用インスタンスの名前です。{{site.data.keyword.Bluemix}} インスタンスのサブドメイン名はオンボード時に割り当てられています。</dd>
</dl>

## 新規サービスの登録

新規サービスを登録するには、以下の API とコード・サンプルを使用してください。

### 経路
{: #registerroute}

```
POST /codi/v1/serviceBrokers
```
{: screen}

### 要求
{: #registerrequest}

| **名前** | **説明** |
|-----------------|-------------------|
| name | サービス・ブローカーの名前。  |
| auth_username | サービス・ブローカーとの接続に使用されるユーザー名。 |
| auth_password | サービス・ブローカーとの接続に使用されるパスワード。 |
| broker_url | サービス・ブローカーとの接続に使用される URL。 |
| owningOrganization | サービスをホワイトリスト登録する初期組織。 |

*表 6. フィールド*

#### 本文
{: #registerbody}

```
{
  "name" : "Service broker's name",
  "auth_username" : "username",
  "auth_password" : "password",
  "broker_url" : "https://broker.comp.com",
  "owningOrganization" : "ORG"
}
```
{: screen}

#### ヘッダー
{: #registerheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### 応答
{: #registerresponse}

#### 状況
{: #registerstatus}

```
201 Created
```
{: screen}

#### 本文
{: #registerbody2}

```
{
  "entity": {
    "name": "Service broker's name",
    "broker_url": "https://provision-broker.comp.bluemix.net/bmx/provisioning/brokers/2063580064-8f23230c-7f36-4ce5-a298-2ab4108f1120",
    "auth_username": "username",
    "space_guid": null
  },
  "warnings": [],
  "metadata": {
    "guid": "49f3adcc-ecc2-46fa-83c1-03322f04b3b1",
    "created_at": "2015-12-07T19:51:50Z",
    "updated_at": null,
    "url": "/v2/service_brokers/49f3adcc-ecc2-46fa-83c1-03322f04b3b1"
  }
}
```
{: screen}

## サービスの更新

サービスを更新するには、以下の API とコード・サンプルを使用してください。

### 経路
{: #updateroute}

`PUT /codi/v1/serviceBrokers`
{: screen}

### 要求
{: #updaterequest}

| **名前** | **説明** |
|-----------------|-------------------|
| name | サービス・ブローカーの名前。 この名前は、サービスを作成するために使用した名前から変更できません。 |
| auth_username | サービス・ブローカーとの接続に使用されるユーザー名。 |
| auth_password | サービス・ブローカーとの接続に使用されるパスワード。 |
| broker_url | サービス・ブローカーとの接続に使用される URL。 |
| owningOrganization | サービスをホワイトリスト登録する初期組織。 |

*表 7. フィールド*

#### 本文
{: #updatebody}

```
{
  "name" : "Service Broker's name",
  "auth_username" : "username",
  "auth_password" : "newPassword",
  "broker_url" : "https://broker.comp.com",
  "owningOrganization" : "ORG"
}
```
{: screen}

#### ヘッダー
{: #updateheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### 応答
{: #updateresponse}

#### 状況
{: #updatestatus}

```
201 Created
```
{: screen}

#### 本文
{: #updatebody2}

```
{
  "entity": {
    "name": "Service Broker's name",
    "broker_url": "https://provision-broker.dys0.bluemix.net/bmx/provisioning/brokers/2063580064-d11bdd84-7556-469f-858d-2098b531f7f2",
    "auth_username": "username",
    "space_guid": null
  },
  "warnings": [],
  "metadata": {
    "guid": "2cbdb812-d37f-443b-894a-a96de31e5c38",
    "created_at": "2015-12-07T20:11:08Z",
    "updated_at": "2015-12-07T20:11:19Z",
    "url": "/v2/service_brokers/2cbdb812-d37f-443b-894a-a96de31e5c38"
  }
}
```
{: screen}

## サービスの削除

サービスを削除するには、以下の API とコード・サンプルを使用してください。

| **名前** | **説明** |
|-----------------|-------------------|
| name | サービス・ブローカーの名前。 この名前は、サービスを作成するために使用した名前から変更できません。 |

*表 8. パラメーター*

### 経路

```
DELETE /codi/v1/serviceBrokers?name=name of service broker
```
{: screen}

### 要求
{: #deleterequest}

#### ヘッダー
{: #deleteheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### 応答
{: #deleteresponse}

#### 状況
{: #deletestatus}

```
204 No Content
```
{: screen}

## CF CLI を使用したユーザーの管理
{: #usingadmincli}

Cloud Foundry コマンド・ライン・インターフェースと {{site.data.keyword.Bluemix_notm}} 管理 CLI プラグインを使用することで、{{site.data.keyword.Bluemix_notm}} 環境のユーザーを管理できます。例えば、LDAP レジストリーからユーザーを追加できます。

最初に、CF コマンド・ライン・インターフェースをインストールします。{{site.data.keyword.Bluemix_notm}} 管理 CLI プラグインを使用する場合、CF バージョン 6.11.2 以降が必要です。[Cloud Foundry コマンド・ライン・インターフェースのダウンロード](https://github.com/cloudfoundry/cli/releases){: new_window}

**制限:** Cloud Foundry コマンド・ライン・インターフェースは、Cygwin ではサポートされていません。Cloud Foundry コマンド・ライン・インターフェースは Cygwin コマンド・ライン・ウィンドウ以外のコマンド・ライン・ウィンドウで使用してください。

### {{site.data.keyword.Bluemix_notm}} 管理 CLI プラグインの追加

CF コマンド・ライン・インターフェースをインストール後、{{site.data.keyword.Bluemix_notm}} 管理 CLI プラグインを追加できます。

**注**: 既に {{site.data.keyword.Bluemix_notm}} 管理プラグインをインストール済みの場合、プラグインをアンインストールし、リポジトリーを削除してから、再インストールして最新の更新を取得することが必要になる場合があります。

以下のステップを実行して、リポジトリーを追加し、プラグインをインストールします。


<ol>
<li>{{site.data.keyword.Bluemix_notm}} 管理プラグイン・リポジトリーを追加するには、以下のコマンドを実行します:<br/><br/> <code>
cf add-plugin-repo BluemixAdmin https://console.&lt;subdomain&gt;.bluemix.net/cli
</code><br/><br/>
<dl class="parml">
<dt class="pt dlterm">&lt;subdomain&gt;</dt>
<dd class="pd">ご使用の {{site.data.keyword.Bluemix_notm}} インスタンス用 URL のサブドメインです。</dd>
</dl>
</li>
<li>{{site.data.keyword.Bluemix_notm}} 管理 CLI プラグインをインストールするには、以下のコマンドを実行します:<br/><br/> <code>
cf install-plugin bluemix-admin-cli -r BluemixAdmin
</code>
</li>
</ol>

コマンドのリストを表示するには、次のコマンドを実行します。


`cf plugins`
{: codeblock}

追加でコマンドのヘルプを表示するには、`-help` オプションを使用します。

{{site.data.keyword.Bluemix_notm}} 管理 CLI プラグインを使用した作業方法について詳しくは、『[{{site.data.keyword.Bluemix_notm}} 管理](../cli/plugins/bluemix_admin/index.html)』を参照してください。
