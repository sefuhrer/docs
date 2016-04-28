---

 

copyright:

  years: 2015，2016

 

---

{:shortdesc: .shortdesc} 
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:screen: .screen}

#在 {{site.data.keyword.Bluemix_notm}} 中托管应用程序

*上次更新时间：2015 年 12 月 1 日*

<!--The whole topic is staging only -->

通过 {{site.data.keyword.Bluemix}}，可以创建应用程序以及托管现有应用程序。
只要 {{site.data.keyword.Bluemix_notm}} 是云就绪型的，就可以将应用程序迁移到其中。{{site.data.keyword.Bluemix_notm}} 为您提供了各种运行应用程序的方法，例如 Cloud Foundry、IBM Containers 和虚拟机。

##使应用程序成为云就绪型应用程序
{: #cloud-readyapps}

云就绪型应用程序在设计和构建应用程序时遵循云平台原则。云就绪型应用程序可以使用云平台提供的各项功能。

如果应用程序中遵循了以下所有原则，那么该应用程序即为云就绪型，且可以迁移到 {{site.data.keyword.Bluemix_notm}}。如果应用程序违反了某个原则，那么通常可以将应用程序修改为遵循原则。

* 不将应用程序直接编码成特定拓扑。

  在非云环境中，应用程序可能会使用特定的部署拓扑。但因为云就绪型应用程序和服务允许进行即时可扩展性更改，所以该应用程序拓扑在云应用程序中可能会更改。可扩展性更改包括动态扩展和手动调整应用程序实例数。

  在构建应用程序时，应尽可能使其通用且无状态，以避免应用程序受到可扩展性更改的影响。

* 不要假定本地文件系统是永久性的。

  由于在云上应用程序实例可以随时移动、删除或复制，因此不要依赖于写入文件系统的文件。如果应用程序使用本地文件系统作为存储频繁使用的信息（包括应用程序日志）的高速缓存，那么关闭实例并在其他位置或其他 VM 中重新启动该实例时，这些信息会丢失。

  可以将此类信息存储在服务中，例如 SQL 或 NoSQL 数据库，而不是存储在本地文件系统中。在动态云环境中，还必须使日志在比生成日志的应用程序实例生命周期更长的服务上可用。

* 不要在应用程序中存储会话状态。

  系统状态是由数据库和共享存储器定义的，而不是由每个单独的运行中的应用程序实例定义的。无论哪种具有状态的形式，都会限制应用程序的可扩展性。尝试通过将会话状态存储在服务器的集中位置，可使会话状态的影响降至最低。

  如果无法完全消除会话状态的影响，请将其推出到应用程序服务器外部的高可用性存储。这些存储包括 IBM WebSphere Extreme Scale、Redis、Memcached 或外部数据库。

* 不要使用特定基础架构依赖关系。

  此通用原则具有多种表示。例如，不要假定应用程序使用的服务分配有特定主机名或 IP 地址。由于服务可能会在云环境中重新定位或重新生成，因此主机名和 IP 地址也会更改。

  将特定于环境的依赖关系抽取到一组属性文件中是一种改进，但这仍然不够。
最佳做法是使用外部服务注册表来解析服务端点，或者通过虚拟名称将整个路由功能委派给服务总线或负载均衡器。

* 不要在应用程序中使用基础架构 API。

  如果在应用程序中依赖特定的基础架构 API，那么因为基础架构 API 可能会引用软件堆栈中的许多不同层，所以要更改基础架构会变得更为困难。

  可以改为依赖现有开放式源代码或商业产品，并将 PaaS 解决方案保留在 PaaS 层中以使其不受应用程序代码影响。

* 不要使用模糊协议。

  不要使用需要额外配置才能实现弹性的模糊协议。

  基于标准协议的应用程序使用委派给平台的配置项，因而弹性更大。标准协议包括 HTTP、SSL、标准数据库、排队和 Web Service 连接。

* 不要依赖于特定于操作系统的功能。

  如果已经使用了特定于操作系统的功能，那么可以通过兼容性库（例如，Cygwin 和 Mono）来解决此问题。Cygwin 是一种兼容性库，用于在 Windows 环境中提供一组 Linux 工具。Mono 是一种兼容性库，用于在 Linux 中提供 Windows .NET 功能。

  避免特定于操作系统的依赖关系；请改为使用中间基础架构或服务提供者提供的服务。

* 不要手动安装应用程序。

  在动态云环境中，可能会根据需要频繁安装应用程序。安装过程必须编制成脚本并且必须可靠，而且配置数据必须已从脚本进行了外部化。

  至少应将应用程序安装作为一组独立于操作系统的统一脚本进行捕获。使应用程序安装保持在较小规模且可移植，以适应不同的自动化方法。此外，尽可能减少应用程序安装需要的依赖关系。

有关云就绪型应用程序的更多信息，请参阅 [The 12-factor application](http://12factor.net/){:new_window}。

##迁移应用程序
{: #ht_hostapp}

您可以将应用程序以递增方式迁移到 {{site.data.keyword.Bluemix_notm}}，而不是将应用程序完全转移到云环境。可以使用 Cloud Integration 服务先迁移应用程序的一部分，并连接到现有数据或记录系统。

在云应用程序中，可能需要访问后端数据或服务，例如记录系统。在 {{site.data.keyword.Bluemix_notm}} 中，可以使用 Secure Gateway 服务在 {{site.data.keyword.Bluemix_notm}} 组织和企业后端网络之间建立一条安全的隧道。该服务支持 {{site.data.keyword.Bluemix_notm}} 上的应用程序访问后端网络的数据和服务。有关详细信息，请参阅 [Reaching enterprise backend with Bluemix Secure Gateway via console](https://developer.ibm.com/bluemix/2015/04/01/reaching-enterprise-backend-bluemix-secure-gateway/){:new_window}。

要将应用程序作为 Cloud Foundry 应用程序部署到 {{site.data.keyword.Bluemix_notm}}，请从 {{site.data.keyword.Bluemix_notm}} 目录中选择运行时。运行时包含 Hello World 入门模板应用程序，您可以将其替换为自己的应用程序。如果找不到入门模板来提供所需的运行时，那么可以通过在 cf push 命令中使用 -b 选项，将 Cloud Foundry 兼容的定制 buildpack 添加到 {{site.data.keyword.Bluemix_notm}} 中。有关详细信息，请参阅[使用社区 buildpack](../cfapps/byob.html)。

可以使用 {{site.data.keyword.Bluemix_notm}} 提供的以下工具和服务：

| 工具	| 方法 |
|:------|:--------|
|Cloud Foundry 命令行界面 (cf cli)	|在本地客户机上管理代码，并使用 Cloud Foundry 命令行界面将应用程序手动推送到 {{site.data.keyword.Bluemix_notm}}。
有关更多信息，请参阅[上传应用程序](../starters/upload_app.html)。|
|Eclipse	|在 Eclipse 中管理代码，并使用 IBM Eclipse Tools for {{site.data.keyword.Bluemix_notm}} 来推送应用程序。|
|Git 集成	|在 GitHub 上管理代码，并将 Git 集成到 {{site.data.keyword.Bluemix_notm}}。
可以与其他开发者进行协作。落实代码中的更改时，应用程序将自动部署到 {{site.data.keyword.Bluemix_notm}}。无需手动推送应用程序。|
|{{site.data.keyword.Bluemix_notm}} DevOps Delivery Pipeline	|在 DevOps GitHub 存储库上管理代码，并通过 DevOps Delivery Pipeline 将应用程序部署到 {{site.data.keyword.Bluemix_notm}}。|
*表 1. {{site.data.keyword.Bluemix_notm}} 工具*

如果 Cloud Foundry 平台不支持应用程序要求，那么可以使用通过更多定制选项设置、配置并维护的运行时的容器或 VM。

##使用 cf cli 上传应用程序
{: #ht_cfcli}

可以在本地客户机上管理代码，并使用 Cloud Foundry 命令行界面将应用程序手动上传到 {{site.data.keyword.Bluemix_notm}}。
如果更改了代码，必须将应用程序重新推送到 {{site.data.keyword.Bluemix_notm}} 才能运行更新后的代码。

执行以下步骤来迁移应用程序：

<ol>
<li>安装 Cloud Foundry 命令行界面。确保使用最新版本的 cf 命令行界面。<ol>
<li>下载针对您操作系统的安装程序。</li>
<li>遵循工具向导来安装命令行。</li>
<li>使用以下命令来验证 cf 命令行界面的版本：<pre>cf -v</pre></li>
</ol>
</li>

<li>可选：如果想要在将应用程序推送到 {{site.data.keyword.Bluemix_notm}} 之前指定并保存部署详细信息，那么可以通过执行以下步骤来添加应用程序清单：<ol>
<li>转至应用程序的工作目录，然后创建名为 manifest.yml 的文件，此为缺省名称。</li>
<li>在清单文件中指定部署详细信息。以下示例显示了 Java™ 应用程序的清单文件。<pre class="pre codeblock"><code>applications:
- disk_quota: 1024M
  host: myjavatest
  name: MyJavaTest
  path: webStarterApp.war
  domain: mybluemix.net
  instances: 1
  memory: 512M</code></pre>
<p>有关可以在此文件中使用的受支持选项的更多信息，请参阅[应用程序清单](../manageapps/depapps.html#appmanifest)。</p></li></ol>
</li>

<li>推送应用程序。可以使用 cf push 命令上传应用程序。<ol>
<li>通过运行以下命令来连接并登录到 {{site.data.keyword.Bluemix_notm}}。系统提示时，选择组织和空间。<pre>cf login -a https://api.ng.bluemix.net</pre></li>
<li>从应用程序目录中，输入带有应用程序名称的 cf push 命令。应用程序名称在 {{site.data.keyword.Bluemix_notm}} 环境中必须唯一。<pre>cf push appname 
</pre></li>
<li>可选：如果使用外部 buildpack，那么必须在 cf push 命令中使用 -b 选项。例如：<pre>cf push appname -b buildpack_URL</pre>
<p>请参阅“使用社区 buildpack”以获取详细信息。</p>
</li></ol>
</li>

<li>可选：如果更改了应用程序，那么必须重新输入 cf push 命令来上传这些更改。cf 命令行界面会使用您先前的选项以及您对提示的响应来通过新的代码段更新应用程序正在运行的任何实例。</li>
</ol>

**注：**

* 使用 cf push 命令时，cf 命令行界面会将当前目录中的所有文件和目录复制到 {{site.data.keyword.Bluemix_notm}} 中。确保应用程序目录中只包含必需的文件。
* 确保组织的内存足够供应用程序的所有实例使用。要查看组织的内存配额，请使用 cf org org_name。
* 有关 cf push 的更多信息，请参阅 [cf 命令](../cli/reference/cfcommands/index.html)。

##迁移数据和使用服务
{: #ht_service}

将应用程序上传到 {{site.data.keyword.Bluemix_notm}} 后，从 {{site.data.keyword.Bluemix_notm}} 目录中选择该应用程序连接到的服务，创建服务实例，将实例绑定到该应用程序，然后重新启动该应用程序。

应用程序的 VCAP_SERVICES 环境变量是一种 JSON 对象，包含有关如何与 {{site.data.keyword.Bluemix_notm}} 中的服务实例进行交互的信息。
这些信息包含服务实例名称、凭证和服务实例的连接 URL。

要在 {{site.data.keyword.Bluemix_notm}} 中运行代码，必须添加用于解析 VCAP_SERVICES 变量以获取有关服务连接的信息的代码逻辑。修改应用程序以获取通过环境变量以动态方式分配的服务实例的主机和端口。以下示例显示了如何获取 Ruby 应用程序中 Postgre SQL 服务实例的凭证：

```
services = JSON.parse(ENV['VCAP_SERVICES'], :symbolize_names => true)

        url = services.values.map do |srvs|
          srvs.map do |srv|
            if srv[:credentials][:uri] =~ /^postgres/
              srv[:credentials][:uri]
            else
              []
            end
          end
        end.flatten!.first
```		
{:codeblock}

要确保应用程序可以在本地环境中运行，请在修改 {{site.data.keyword.Bluemix_notm}} 的应用程序后，检查是否存在为所有 {{site.data.keyword.Bluemix_notm}} Cloud Foundry 应用程序设置的 VCAP_SERVICES 环境变量。


# 相关链接
## 常规 
* [IBM Containers](../containers/container_cli_ov.html)
* [虚拟机](../virtualmachines/vm_index.html)
* [Delivery Pipeline 入门](../services/DeliveryPipeline/index.html)
* [使用 IBM Eclipse Tools for Bluemix 部署应用程序](../manageapps/eclipsetools/eclipsetools.html)
* [twelve-factor app](http://12factor.net/){:new_window}
* [Reaching enterprise backend with Bluemix Secure Gateway via console](https://developer.ibm.com/bluemix/2015/04/01/reaching-enterprise-backend-bluemix-secure-gateway/){:new_window}
