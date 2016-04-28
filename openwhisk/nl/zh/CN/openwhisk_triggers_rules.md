---

 

copyright:

  years: 2016

 

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# 创建触发器和规则
{: #openwhisk_triggers}
*上次更新时间：2016 年 2 月 22 日*

{{site.data.keyword.openwhisk}} 触发器和规则为平台带来了事件驱动型功能。来自外部和内部事件源的事件将通过触发器进行传递，并且规则允许操作对这些事件做出反应。
{: shortdesc}

## 触发器

触发器是为某类事件指定的通道。下面是触发器示例：
- 位置更新事件的触发器。
- 关于文档上传到 Web 站点的触发器。
- 传入电子邮件的触发器。

触发器可以使用键/值对的字典来*触发*（激活）。有时，此字典称为*事件*。与操作一样，每次触发触发器都会生成一个激活标识。

触发器可以由用户显式触发，也可以由外部事件源代表用户触发。
通过*订阅源*，可以方便地配置外部事件源来触发 {{site.data.keyword.openwhisk_short}} 可使用的触发器事件。下面是订阅源的示例：
- Cloudant 数据更改订阅源，每次在数据库中添加或修改文档时，触发触发器事件。
- Git 订阅源，针对 Git 存储库中的每次落实，触发触发器事件。

## 规则

规则用于将一个触发器与一个操作关联在一起，每次触发触发器时，都会将触发器事件作为输入来调用相应的操作。

使用相应的规则集时，可以通过单个触发器事件来调用多个操作，也可以调用一个操作以响应来自多个触发器的事件。

例如，假设一个系统包含以下操作：
- `classifyImage` 操作，用于检测图像中的对象并对其进行分类。
- `thumbnailImage` 操作，用于创建图像的缩略图版本。

此外，假设有两个事件源将触发以下触发器：
- `newTweet` 触发器，在发布新推文时触发。
- `imageUpload` 触发器，在将图像上传到 Web 站点时触发。

可以设置规则，以使单个触发器事件调用多个操作，并使多个触发器调用同一操作：
- `newTweet -> classifyImage` 规则。
- `imageUpload -> classifyImage` 规则。
- `imageUpload -> thumbnailImage` 规则。

这三个规则确定了以下行为：对推文中的图像和上传的图像分类，对上传的图像分类，以及生成缩略图版本。 

## 创建并触发触发器
{: #openwhisk_triggers}

触发器可以在发生特定事件时触发，也可以手动触发。

例如，创建触发器来发送用户位置更新，然后手动触发该触发器。

1. 输入以下命令来创建触发器：
 
  ```
  wsk trigger create locationUpdate
  ```
  {: pre}
 
  ```
  ok: created trigger locationUpdate
  ```
  {: screen}

2. 通过列出触发器集来检查是否已创建该触发器。

  ```
  wsk trigger list
  ```
  {: pre}
 
  ```
  triggers
  /someNamespace/locationUpdate                            private
  ```
  {: screen}

  到目前为止，您已创建可向其触发事件的指定“通道”。

3. 接下来，通过指定触发器名称和参数来触发触发器事件：

  ```
  wsk trigger fire locationUpdate --param name "Donald" --param place "Washington, D.C."
  ```
  {: pre}

  ```
  ok: triggered locationUpdate with id fa495d1223a2408b999c3e0ca73b2677
  ```
  {: screen}

   您向 statusUpdate 触发器触发的任何事件当前并不执行任何操作。要发挥作用，该触发器需要规则来将其与操作关联在一起。


## 使用规则关联触发器和操作
{: #openwhisk_rules}

规则用于将触发器与操作关联在一起。每次触发触发器事件时，都会通过事件参数来调用操作。

例如，创建一个规则，用于在每次发布位置更新时都调用 hello 操作。 

1. 通过我们将使用的操作码来创建“hello.js”文件：```
  function main(params) {
     return {payload:  'Hello, ' + params.name + ' from ' + params.place};
  }
  ```
  {: codeblock}

2. 确保该触发器和操作存在。```
  wsk trigger update locationUpdate
  ```
  {: pre}
  
  ```
  wsk action update hello hello.js
  ```
  {: pre}

3. 创建并启用规则。三个参数分别是规则名称、触发器和操作。```
  wsk rule create --enable myRule locationUpdate hello
  ```
  {: pre}

4. 触发 locationUpdate 触发器。每次触发事件时，都会通过事件参数来调用 hello 操作。```
  wsk trigger fire locationUpdate --param name "Donald" --param place "Washington, D.C."
  ```
  {: pre}
  
  ```
  ok: triggered locationUpdate with id d5583d8e2d754b518a9fe6914e6ffb1e
  ```
  {: screen}

5. 通过检查最新的激活来验证是否调用了该操作。```
  wsk activation list --limit 1 hello
  ```
  {: pre}
  
  ```
  activations
  9c98a083b924426d8b26b5f41c5ebc0d             hello
  ```
  {: screen}
  
  ```
  wsk activation result 9c98a083b924426d8b26b5f41c5ebc0d
  ```
  {: pre}
  ```
  {
     "payload": "Hello, Donald from Washington, D.C."
  }
  ```
  {: screen}

  您将看到 hello 操作收到了事件有效内容，并返回了期望的字符串。

  可以创建多个规则，用于将同一触发器与不同操作相关联。
