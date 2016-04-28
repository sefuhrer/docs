---

copyright:
  years: 2015, 2016

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# 環境変数
{: #environment_variables}

*最終更新日時: 2016 年 3 月 23 日*

Liberty for Java によってサポートされる環境変数。

<table>
<tr>
<th align="left">名前</th>
<th align="left">説明</th>
</tr>

<tr>
<td>BLUEMIX_APP_MGMT_ENABLE</td>
<td>[アプリケーション管理ユーティリティー](../../manageapps/app_mng.html)を使用可能にします</td>
</tr>

<tr>
<td>BLUEMIX_APP_MGMT_INSTALL</td>
<td>[アプリケーション管理ユーティリティー](../../manageapps/app_mng.html)をインストールします</td>
</tr>

<tr>
<td>IBM_LIBERTY_BETA</td>
<td>[Liberty ベータ・フィーチャー](usingBetaFeatures.html)を使用可能にします</td>
</tr>

<tr>
<td>JAVA_OPTS</td>
<td>[Java オプション](customizingJRE.html)を設定します</td>
</tr>

<tr>
<td>JBP_CONFIG_DYNATRACEAGENT</td>
<td>[Dynatrace エージェント・ロケーション情報](dynatrace.html#configuring_liberty_app)を構成します</td>
</tr>

<tr>
<td>JBP_CONFIG_IBMJDK </td>
<td>[IBM JRE バージョン](customizingJRE.html)を構成します</td>
</tr>

<tr>
<td>JBP_CONFIG_LIBERTY</td>
<td>[WAR ファイルまたは EAR ファイル用のフィーチャー](optionsForPushing.html#stand_alone_apps)を含めて、さまざまな Liberty ランタイム・オプションを構成します</td>
</tr>

<tr>
<td>JBP_CONFIG_OPENJDK</td>
<td>[OpenJDK バージョン](customizingJRE.html)</td>を構成します。</tr>

<tr>
<td>JBP_CONFIG_SPRINGAUTORECONFIGURATION </td>
<td>Spring Auto-Reconfiguration フレームワークを使用不可にします。使用不可にするには、値を enabled: false に設定します。</td>
</tr>

<tr>
<td>JBP_LOG_LEVEL</td>
<td>ビルドパックのロギング・レベルを設定します。可能な値: <b>DEBUG</b>、<b>INFO</b> (デフォルト)、<b>WARN</b>、<b>ERROR</b>、または <b>FATAL</b></td>
</tr>

<tr>
<td>JVM</td>
<td>[JRE タイプ](customizingJRE.html)を選択します</td>
</tr>

<tr>
<td>JVM_ARGS</td>
<td>[JVM 引数](customizingJRE.html)を設定します</td>
</tr>

<tr>
<td>HTTP_PROXY</td>
<td>プロキシー・サーバー情報を設定します</td>
</tr>

<tr>
<td>HTTPS_PROXY</td>
<td>プロキシー・サーバー情報を設定します</td>
</tr>

<tr>
<td>services_autoconfig_excludes</td>
<td>サービスの[自動構成](autoConfig.html#opting_out)を使用不可にします。</td>
</tr>
</table>

# 関連リンク
## 一般
* [Liberty ランタイム](index.html)
* [Liberty プロファイル概要](http://www-01.ibm.com/support/knowledgecenter/SSAW57_8.5.5/com.ibm.websphere.wlp.nd.doc/ae/cwlp_about.html)
