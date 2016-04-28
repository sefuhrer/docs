---

 

copyright:

  years: 2015，2016

 

---

{:shortdesc: .shortdesc} 
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:screen: .screen}

# シナリオ: エンドツーエンド開発
{: #ee}

*最終更新日: 2015 年 11 月 6 日*

アプリを作成、実行、およびデプロイするときに、{{site.data.keyword.Bluemix}} ユーザー・インターフェース、プラットフォーム、および各種ツールを使用できます。このエンドツーエンド開発シナリオに従って作業を開始してください。
{:shortdesc}

## サインアップ
{: #ee_start}

開始するには、その前に [https://console.ng.bluemix.net/](https://console.ng.bluemix.net/) からサインアップして IBM ID を取得する必要があります。その後、{{site.data.keyword.Bluemix_notm}} にログインし、30 日間の無料トライアルを開始します。{{site.data.keyword.Bluemix_notm}} の無料トライアルでは、2 GB のランタイム・メモリーと 10 個のサービス・インスタンスを使用できます。

## {{site.data.keyword.Bluemix_notm}} ユーザー・インターフェースを使用した Web アプリの作成
{: #ee_appui}

サインアップした後、最初のアプリの作成を {{site.data.keyword.Bluemix_notm}} ユーザー・インターフェースを使用して開始します。

{{site.data.keyword.Bluemix_notm}} では、アプリは組織およびスペースに関連付けられます。1 つの組織を複数のコラボレーターが所有し、使用します。最初は、ユーザー名を元に名付けられたデフォルトの組織が 1 つ用意され、自身が唯一のコラボレーターになります。この組織内にスペースも 1 つ用意されます。スペースはアプリを実行するための環境です。例えば、開発環境として dev というスペース、テスト環境として test というスペース、実稼働環境として production というスペースを作成できます。さらに、各環境は地域に属します。{{site.data.keyword.Bluemix_notm}} では、少ないネットワーク待ち時間、データ・プライバシー、高い可用性のために、アプリケーションを特定の地域にデプロイできます。詳細については、『地域』を参照してください。

このシナリオでは、Node.js を使用して Web アプリを開発します。開発者は米国にいて、このアプリのユーザーの大部分も米国にいるものとします。ネットワーク待ち時間を少なくできるように、ユーザー・ベースの近くでアプリの作成と実行を行うことに決めます。{{site.data.keyword.Bluemix_notm}} にログインした後、ユーザー・インターフェースの右上隅で**「米国南部 (US South)」**地域を選択します。次に、以下の手順を実行してアプリを作成します。
  1. **「アプリの作成」**をクリックします。
  2. **「Web」**を選択します。
  3. 作成する Web アプリのために Node.js 用スターター SDK を選択し、**「続行」**をクリックします。
  4. アプリ名として固有の名前 (例えば TestNode) を入力し、**「完了」**をクリックします。このアプリ名は {{site.data.keyword.Bluemix_notm}} 環境全体で固有でなければなりません。
  
これで、**「コーディングの開始」**の手順を表示できるようになります。この手順に従って、TestNode のスターター・コードをダウンロードし、変更し、デプロイできます。

アプリには、1 つのインスタンスと 512 MB のメモリー割り当て量がデフォルトで割り当てられます。例えば、3 つのインスタンスで、インスタンス当たり 1 GB メモリーにするなど、メモリーを増やしたりインスタンスを追加したりしてアプリの可用性を高めることができます。アプリのインスタンス数およびメモリー割り当て量を指定するには、**「アプリの概要の表示」**をクリックします。例えば、インスタンス数に 3、メモリー割り当て量に 1 GB と入力し、**「保存」**をクリックします。また、問題のトラブルシューティングのために、ファイル、ログ、および環境変数を表示することもできます。

## {{site.data.keyword.Bluemix_notm}} ユーザー・インターフェースを使用したサービスのバインド
{: #ee_bindui}

アプリを作成した後、アプリとデータベースを接続します。こうすることで、データベース照会言語を使用してアプリ・データを保管および監視できるようになります。このシナリオでは、{{site.data.keyword.Bluemix_notm}} によって提供されている {{site.data.keyword.cloudant}} サービスを使用します。

アプリケーション内でサービスを使用するには、以下の手順を実行して、サービス・インスタンスを作成し、そのサービス・インスタンスにアプリケーションをバインドする必要があります。
  1. アプリの「概要」ページで**「サービスまたは API の追加」**をクリックします。
  2. {{site.data.keyword.Bluemix_notm}} カタログで、{{site.data.keyword.cloudant}} サービスを選択します。
  3. サービス・インスタンスの固有の名前を入力するか、または {{site.data.keyword.Bluemix_notm}} によって生成されるデフォルト名を使用し、**「作成」**をクリックします。
  4. 「アプリケーションの再ステージ」ウィンドウが表示されます。**「再ステージ」**をクリックしてアプリを再ステージします。
  
これで、アプリが {{site.data.keyword.cloudant}} サービスにバインドされました。アプリケーションがサービス・インスタンスと通信するためのすべての必要なデータは VCAP_SERVICES 環境変数に入っています。例えば、{{site.data.keyword.Bluemix_notm}} はいくつかのアプリケーションを同じ仮想マシン上でホストしているため、複数のアプリケーションが同じ HTTP ポート番号を使用して着信要求を受け取ることはできません。競合を避けるため、各アプリケーションに固有のポート番号が与えられます。このポート番号は VCAP_APP_PORT 変数の下にあります。

詳細については、アプリの「概要」ページで**「環境変数」**をクリックして、VCAP_SERVICES の完全なリストを表示してください。
```
{
   "cloudantNoSQLDB": [
      {
         "name": "Cloudant NoSQL DB-tx",
         "label": "cloudantNoSQLDB",
         "plan": "Shared",
         "credentials": {
            "username": "d72837bb-b341-4038-9c8e-7f7232916197-bluemix",
            "password": "b6fc4708942b70a88853177ee52a528d07a43fa8575a69abeb8e044a7b0a7424",
            "host": "d72837bb-b341-4038-9c8e-7f7232916197-bluemix.cloudant.com",
            "port": 443,
            "url": "https://d72837bb-b341-4038-9c8e-7f7232916197-bluemix:b6fc4708942b70a88853177ee52a528d07a43fa8575a69abeb8e044a7b0a7424@d72837bb-b341-4038-9c8e-7f7232916197-bluemix.cloudant.com"
         }
      }
   ]
}
```

**注:** この環境変数は 1 つの JSON オブジェクトの直列化であり、アプリがバインドされているサービス・インスタンスごとに 1 つの項目があります。各サービス・インスタンスが提供するデータの量とタイプはサービス固有です。アプリがサービスを何も使用しない場合、VCAP_SERVICES は空の JSON オブジェクトです。この環境変数は、サービスをアプリに追加する場合にのみ使用されます。

## cf cli を使用したアプリのビルド
{: #ee_cf}

{{site.data.keyword.Bluemix_notm}} では、例えば cf コマンド・ライン・インターフェースや Eclipse ツールなど、アプリでコーディングを始めるためのいくつかのツールが提供されています。TestNode アプリでのコーディングを始めるために cf コマンド・ライン・インターフェースを選択できます。

  1. 最初に、アプリのコードをダウンロードして開発します。
  
    1. アプリの「コーディングの開始」ページに移動します。**「スターター・コードのダウンロード」**ボタンをクリックして、アプリのコードをダウンロードします。
    2. ダウンロードしたファイルをディレクトリー (例えば `C:&#xa5;test`) に解凍します。
    3. ローカル統合開発環境でコードを開発します。
	
  2. **cf** コマンド・ライン・インターフェース (CLI) をインストールします。
  
    1. ご使用のオペレーティング・システム向けの cf コマンド・ライン・ツール・インストール・プログラムをダウンロードします。
    2. ツールのウィザードに従ってインストールを実行します。
    3. **cf -v** コマンドを使用して、cf コマンド・ライン・インターフェースのバージョンを確認します。例えば次のようにします。
	
	```
	cf -v
	```
	
    **要件:** 常に最新バージョンの cf コマンド・ライン・ツールを使用するようにしてください。
  3. **cf** コマンド・ライン・インターフェースをインストールした後、**cf api** コマンドを使用して、作業する {{site.data.keyword.Bluemix_notm}} 地域を指定する必要があります。**cf** コマンド・ライン・インターフェースは *https://api.Bluemix_URL* を使用します (*Bluemix_URL* は地域の URL です)。米国南部地域の URL は ng.bluemix.net です。次のコマンドを入力して、{{site.data.keyword.Bluemix_notm}} に接続します。
  
  ```
  cf api https://api.ng.bluemix.net
  ```
  
  他の {{site.data.keyword.Bluemix_notm}} 地域への接続について詳しくは、『{{site.data.keyword.Bluemix_notm}} 地域』を参照してください。{{site.data.keyword.Bluemix_notm}} 地域を指定すると、指定したロケーション情報が保存されます。
  
  4. 次に、cf login コマンドを使用して {{site.data.keyword.Bluemix_notm}} にログインできます。
  
  ```
  cf login -u your_user_ID -p ***** -o your_org_name -s your_space_name
  ```
  
  5. {{site.data.keyword.Bluemix_notm}} にログインすると、アプリを {{site.data.keyword.Bluemix_notm}} にデプロイする準備ができている状態になります。アプリのディレクトリー `C:&#xa5;test` から、次のコマンドを入力します。
  
  ```
  cf push TestNode
  ```
  
  **cf push** コマンドについて詳しくは、『アプリのアップロード』を参照してください。
  
  6. これで、ブラウザーで以下のアプリ URL を入力することによってアプリにアクセスできるようになりました。
  ```
  http://TestNode.mybluemix.net
  ```

アプリをビルドするために他のツール (Eclipse ツールなど) を選択することもできます。詳細については、{{site.data.keyword.Bluemix_notm}} ユーザー・インターフェースのアプリの「コーディングの開始」ページを参照してください。

## cf cli を使用したサービスのバインド
{: #ee_cfbind}

{{site.data.keyword.Bluemix_notm}} では、このシナリオで前述したとおり、Bluemix ユーザー・インターフェースを使用してサービスを追加できます。しかし、**cf** コマンド・ライン・インターフェースを使用することでもサービスをバインドできます。cf コマンド・ライン・インターフェースを使用して {{site.data.keyword.cloudant}} サービスを TestNode アプリに追加したいと想定します。

アプリ内で {{site.data.keyword.cloudant}} サービスを使用するには、Cloudant サービス・インスタンスを作成し、そのサービス・インスタンスにアプリをバインドし、その後でそのサービス・インスタンスを使用する必要があります。他のすべてのサービスにも同じ手順が適用されます。

  1. Cloudant NoSQL DB サービス・インスタンスを作成します。
  
  cf create-service コマンドを使用して、サービスの新規インスタンスを作成します。例えば次のようにします。
  
  ```
  cf create-service cloudantNoSQLDB Shared cloudant100
  ```
  
  cf services コマンドを使用して、作成したサービス・インスタンスのリストを表示することもできます。
  
  ```
  cf services```
  
  サービス・インスタンスが作成されると、そのサービス・インスタンスは任意のアプリケーションでバインドおよび使用することができます。
  
  2. サービス・インスタンスをアプリにバインドします。
  
  サービス・インスタンスを使用するには、それをアプリケーションにバインドする必要があります。アプリケーション名および作成したサービス・インスタンスを指定することによって、cf bind-service コマンドを使用してサービス・インスタンスをアプリケーションにバインドします。
  
  ```
  cf bind-service TestNode cloudant100
  ```
  
  サービス・インスタンスをアプリケーションにバインドすると、{{site.data.keyword.Bluemix_notm}} はサービスと通信できるようになり、新規アプリケーションがそのサービス・インスタンスと通信することを指定できます。異なるサービスに対して、{{site.data.keyword.Bluemix_notm}} はバインド中のアプリケーションおよびサービス・インスタンスの処理方法を変えることがあります。例えば、サービスによっては、サービス・インスタンスと通信する各アプリケーションごとに新規テナントを作成する場合があります。サービスは {{site.data.keyword.Bluemix_notm}} に応答を返すときに、アプリケーションとサービスの間での通信のためにアプリケーションに渡される必要のある情報 (例えば資格情報) を渡します。

  **注:** サービス・インスタンスにバインドされるときにアプリケーションが実行中である場合、VCAP_SERVICES 環境変数はアプリケーションが再始動されるまで更新されません。アプリケーションを再始動するには、cf restart コマンドを使用します。
  
  3. サービス・インスタンスを使用します。
  
  このシナリオでは、VCAP_SERVICES 環境変数には、アプリケーションが {{site.data.keyword.cloudant}} のこのインスタンスに接続するために使用できる以下の項目のような情報が含まれます。
  
  <dl><dt>username</dt>
  <dd>d72837bb-b341-4038-9c8e-7f7232916197-bluemix</dd>
  <dt>password</dt>
  <dd>b6fc4708942b70a88853177ee52a528d07a43fa8575a69abeb8e044a7b0a7424</dd>
  <dt>url</dt>
  <dd>https://d72837bb-b341-4038-9c8e-7f7232916197-bluemix:b6fc4708942b70a88853177ee52a528d07a43fa8575a69abeb8e044a7b0a7424@d72837bb-b341-4038-9c8e-7f7232916197-bluemix.cloudant.com</dd></dt></dl>
  
  例えば、Node.js アプリはこの情報に次のようにアクセスします。
  ```
  if (process.env.VCAP_SERVICES) {
        var env = JSON.parse(process.env.VCAP_SERVICES);
        var cloudant = env['"cloudantNoSQLDB'][0].credentials;
  } else {
        var cloudant = {
                "username" : "user1",
                "password" : "secret",
                "url" : "https://user1:secret@localhost:25002"
                }
        };
  ```
  
  **注:** サンプル・コードで示されているように、{{site.data.keyword.cloudant}} サービス・インスタンスに接続するために、まず最初に VCAP_SERVICES 環境変数が存在するかどうかを確認できます。存在する場合、アプリケーションはこの cloudant 変数のプロパティーを使用してデータベースにアクセスできます。しかし、VCAP_SERVICES 環境変数が存在しない場合、提供されたデフォルト値を持つローカル {{site.data.keyword.cloudant}} サービス・インスタンスが使用されます。
  
  4. サービス・インスタンスと対話します。
  
  資格情報を使用してサービス・インスタンスと対話することができます。実行できるアクションには、読み取り、書き込み、更新などがあります。次の例は、{{site.data.keyword.cloudant}} サービス・インスタンスに JSON オブジェクトを挿入する方法を示しています。
  ```
  // create a new message
var create_message = function(req, res) {
  require('cloudantdb').connect(cloudant.url, function(err, conn) {
    var collection = conn.collection('messages');

    // create message record
    var parsedUrl = require('url').parse(req.url, true);
    var queryObject = parsedUrl.query;
    var name = (queryObject["name"] || 'Bluemix');
    var message = { 'message': 'Hello, ' + name, 'ts': new Date()
};
    collection.insert(message, {safe:true}, function(err){
      if (err) { console.log(err.stack); }
      res.writeHead(200, {'Content-Type': 'text/plain'});
      res.write(JSON.stringify(message));
      res.end('\n');
    });
  });
}
  ```
  
  5. **オプション:** サービス・インスタンスをアンバインドまたは削除します。
  
  サービス・インスタンスが不要になった場合や、一部のスペースを解放したい場合に、サービス・インスタンスのアンバインドまたは削除が必要になることがあります。サービス・インスタンスをアプリからアンバインドするには **cf unbind-service** コマンドを使用し、サービス・インスタンスを削除するには **cf delete-service** コマンドを使用します。

  サービスについて詳しくは、『サービス』を参照してください。{{site.data.keyword.Bluemix_notm}} 環境でアプリケーションを管理するために使用できる **cf** オプションの詳細情報を表示するには、**cf** コマンド・ライン・インターフェースで **cf --help** を実行してください。

  **注:** サービス・インスタンスを削除する前に、もうそれが必要ではないことを確認してください。サービス・インスタンスを削除すると、そのサービス・インスタンスに関連付けられたすべてのデータが消去されます。削除されたサービスにバインドされたアプリケーションの VCAP_SERVICES 環境変数は、アプリケーションが再始動されるまで更新されません。

## アプリのコスト計算
{: #ee_billing}

30 日間の無料トライアルの期限が切れたが、{{site.data.keyword.Bluemix_notm}} を使用し続けることを望んでいるとします。{{site.data.keyword.Bluemix_notm}} を使用し続けるためには、従量課金アカウントまたはサブスクリプション・アカウント用にクレジット・カード情報を追加する必要があります。ただし、{{site.data.keyword.Bluemix_notm}} は、有料アカウントに切り替えた場合でも、ほとんどのランタイム・フレームワークおよびサービスについて無料枠を引き続き提供します。使用量が無料枠を超えない限り、{{site.data.keyword.Bluemix_notm}} による課金はありません。

{{site.data.keyword.Bluemix_notm}} は、アプリのコストを確認できるように、見積もり機能と計算機能を備えています。次のようにして TestNode のコストを確認できます。

  * ダッシュボードで TestNode をクリックします。次に、「概要」ページの右下で**「このアプリのコストの見積もり」**をクリックして **SDK for Node.js** ランタイムおよびサポートの価格を確認し、右上隅でアプリの月の合計価格を確認します。
  
  * あるいは、「価格設定シート」ページで、アプリのランタイムおよびサービスの月次使用量を入力します。例えば、**SDK for Node.js** のインスタンスが 3 つあり、インスタンスごとに 1 GB のメモリーを使用しているといったケースが考えられます。月次価格が計算され、ウィンドウの右上隅に表示されます。

アプリのコストは手動で計算することもできます。そうする場合は、ランタイムおよびサービスの価格を合算してから無料枠を差し引きます。詳しくは、『手動によるコスト計算』を参照してください。

## アプリの削除
{: #ee_removing}

ビルドするアプリが増えるにつれて、割り当て量は限度に近づきます。ただし、もう使用しそうにないアプリが割り当て量を占めているままになっている可能性があります。{{site.data.keyword.Bluemix_notm}} では、いつでも簡単にアプリを削除してスペースを解放することができます。

{{site.data.keyword.Bluemix_notm}} ユーザー・インターフェースで、アプリの「概要」ページに移動し、**「メニュー」**アイコンをクリックし、もう使用しないアプリを削除します。**cf delete** コマンドを使用してアプリを削除することもできます。
