# Android架构蓝图
讨论和展示Android应用的不同架构工具和模式的范例集合

###### 按照国际惯例，提供双语版本的README文档，这里是中文文档(翻译自英文文档)：

#### [英文文档](https://github.com/AweiLoveAndroid/android-architecture/blob/master/README-English.md)|[中文文档](https://github.com/AweiLoveAndroid/android-architecture/blob/master/README.md)

----

<img src="https://github.com/googlesamples/android-architecture/wiki/images/aab-logo.png"/>

Android框架为决定如何 **组织和构建** Android应用程序提供了很大的灵活性。 虽然这种自由是非常有价值的，但它也会导致app具有大量的类;各种不同规则的命名方案，它们跟项目不匹配;或者项目中缺少架构。 这些类型的问题可能使测试，维护和扩展您的app变得困难。

**Android架构蓝图** 项目提供了解决或避免这些常见问题的策略。 该项目使用不同的架构概念和工具实现相同的app。

您可以将此项目中的示例用作学习参考，或作为创建自己的应用程序的起点。 此项目的重点是**演示如何构建代码，设计架构以及采用这些模式对测试和维护应用程序的最终影响**。 您可以通过许多不同方式使用此处演示的技术来构建app。 您自己的特定优先级将影响您在这些项目中实现这些概念的方式，因此您不应将这些示例作为典型示例。 为确保讲解的重心是上述目标，该应用使用简单的用户界面作为演示。

----

## 探索示例

该项目将每个示例应用程序托管在不同的存储库分支中。有关更多信息，请参阅每个分支中的`README.md`文件。

### 稳定的示例
示例 | 描述
-|-
[todo‑mvp](https://github.com/googlesamples/android-architecture/tree/todo-mvp/) | 演示一个基本的 [Model-View-Presenter](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93presenter) (MVP) 体系结构，并为构建其他示例提供了基础。 该示例还可以作为**比较和对比**本项目其他示例的参考。
[todo‑mvp‑clean](https://github.com/googlesamples/android-architecture/tree/todo-mvp-clean/) | 使用 [Clean Architecture](https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html) 的概念。
[todo‑mvp‑dagger](https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/) |使用 [Dagger 2](https://google.github.io/dagger/) 添加对[依赖注入](https://en.wikipedia.org/wiki/Dependency_injection)的支持。
[todo‑mvp‑rxjava](https://github.com/googlesamples/android-architecture/tree/todo-mvp-rxjava/) | 使用 [RxJava 2](https://github.com/ReactiveX/RxJava) 来实现并发性，并抽象数据层。
[todo‑mvvm‑databinding](https://github.com/googlesamples/android-architecture/tree/todo-mvvm-databinding/) | 基于todo-databinding示例，此版本包含 [Model‑View‑ViewModel](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel) 模式。
[todo‑mvvm‑live](https://github.com/googlesamples/android-architecture/tree/todo-mvvm-live/) | 使用[Architecture Components架构组建](https://developer.android.google.cn/topic/libraries/architecture/index.html) 的ViewModels和LiveData以及MVVM架构的Data Binding库。


### 弃用的（过时的）示例

这些示例不再被维护，但它们的实现仍然有效。

示例 | 描述
-|-
[todo‑mvp‑loaders](https://github.com/googlesamples/android-architecture/tree/deprecated-todo-mvp-loaders/) | 使用 [Loaders API](https://developer.android.google.cn/guide/components/loaders.html) 获取数据。
[todo‑databinding](https://github.com/googlesamples/android-architecture/tree/deprecated-todo-databinding/) | 被 [todo‑mvvm‑databinding](https://github.com/googlesamples/android-architecture/tree/todo-mvvm-databinding/) 取代。 
[todo‑mvp‑contentproviders](https://github.com/googlesamples/android-architecture/tree/deprecated-todo-mvp-contentproviders/) | 基于 [todo‑mvp‑loaders](https://github.com/googlesamples/android-architecture/tree/deprecated-todo-mvp-loaders/) 示例，该版本使用Loaders API提取数据，并利用[内容提供者](https://developer.android.google.cn/guide/topics/providers/content-providers.html)。

### 正在开发中的示例

| 示例 | 描述 |
| ------------- | ------------- |
| [dev‑todo‑mvp‑tablet](https://github.com/googlesamples/android-architecture/tree/dev-todo-mvp-tablet/) | 为平板电脑添加主视图和详细视图。 |
| [dev‑todo‑mvvm‑rxjava](https://github.com/googlesamples/android-architecture/tree/dev-todo-mvvm-rxjava/) | 基于todo-rxjava示例，该版本结合了 [Model‑View‑ViewModel](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel) 模式。|
| [dev-todo-mvp-kotlin](https://github.com/googlesamples/android-architecture/tree/dev-todo-mvp-kotlin/) | 将 [todo‑mvp](https://github.com/googlesamples/android-architecture/tree/todo-mvp/) 转换为Kotlin。 |
| [dev-todo-mvvm-live-kotlin](https://github.com/googlesamples/android-architecture/tree/dev-todo-mvvm-live-kotlin/) | 将 [todo‑mvvm‑live](https://github.com/googlesamples/android-architecture/tree/todo-mvvm-live/) 转换成Kotlin。|

有关示例开发的一些计划信息，请参阅[“新示例”问题](https://github.com/googlesamples/android-architecture/issues?q=is%3Aissue+is%3Aopen+label%3A%22New+sample%22)

### 额外的示例

[额外的示例](https://github.com/googlesamples/android-architecture/wiki/External-samples) 是可能与该存储库中其他分支不同步的变体。

| 示例 | 描述 |
| ------------- | ------------- |
| [todo‑mvp‑fragmentless](https://github.com/Syhids/android-architecture/tree/todo-mvp-fragmentless) | 使用 [View](https://developer.android.google.cn/reference/android/view/View.html) 对象代替 [Fragment](https://developer.android.google.cn/reference/android/app/Fragment.html) 对象。|
| [todo‑mvp‑conductor](https://github.com/grepx/android-architecture/tree/todo-mvp-conductor) | 使用 [Conductor](https://github.com/bluelinelabs/Conductor) 框架,使用单个Activity架构重构app。 |
| [todo‑mvi-rxjava](https://github.com/oldergod/android-architecture/tree/todo-mvi-rxjava) | 将 [Model-View-Intent](https://cycle.js.org/model-view-intent.html) 模式适应Android以创建完全reactive架构。 |

----

## 为什么要做一个to-do app？

这个项目中的应用程序旨在简单到足以让您快速理解它，但其复杂程度足以展示难以设计的决策和测试场景。 有关更多信息，请参阅 [应用程序的规范](https://github.com/googlesamples/android-architecture/wiki/To-do-app-specification)。

以下屏幕截图显示了该app的用户界面：

<img src="https://github.com/googlesamples/android-architecture/wiki/images/tasks2.png"/>

----

## 为您的应用选择一个示例

每个示例都包含一个专门的`README.md`文件，在该文件中，你可以找到相关的指标，以及参与者的主观评价和观察。在为你的app选择一个特定的示例时，以下因素值得考虑:

* 你正在开发的应用程序的大小。
* 你的团队的规模和经验。
* 你期望的维修量。
* 你是否需要平板电脑布局。
* 是否需要支持多个平台。
* 你对代码库的紧凑性的偏好。

有关选择和比较样本的更多信息，请参阅以下页面：

* [示例预览](https://github.com/googlesamples/android-architecture/wiki/Samples-at-a-glance)
* [如何对示例进行比较](https://github.com/googlesamples/android-architecture/wiki/How-to-compare-samples)

----

## 在 Android Studio 中打开一个示例

要在Android Studio中打开其中一个示例，首先检查一个示例分支，然后在Android Studio中打开`todoapp /`目录。 以下一系列步骤说明如何打开 [todo-mvp](https://github.com/googlesamples/android-architecture/tree/todo-mvp) 示例。

**注意:** 主分支不编译。

clone克隆库：

    git clone git@github.com:googlesamples/android-architecture.git

Checkout `todo-mvp` 示例:

    git checkout todo-mvp


**注意:** 要查看不同的示例，请用您想要checkout的示例名称替换`todo-mvp`，最后在Android Studio中打开`todoapp /`目录。

----

## 贡献者

该项目由社区**构建**，由Google以及其他核心维护人员策划。

### 额外贡献者

[David González](http://github.com/malmstein) - 核心开发者 (MVP Content Providers sample)

[Karumi](http://github.com/Karumi) - 开发者 (MVP Clean Architecture sample)

[Natalie Masse](http://github.com/freewheelnat) - 核心开发者

[Erik Hellman](https://github.com/ErikHellman) - 开发者 (MVP RxJava sample)

[Saúl Molinero](https://github.com/saulmm) - 开发者 (MVP Dagger sample)

[Mike Nakhimovich](https://github.com/digitalbuddha) - 开发者 (MVP Dagger sample)

[Voicu Klein](https://github.com/kleinsenberg) - 开发者 (MVP RxJava sample)

### 谷歌开发人员

[Jose Alcérreca](http://github.com/JoseAlcerreca) - 主导/核心开发者

[Mustafa Kurtuldu](https://github.com/mustafa-x) - UX/设计

[Stephan Linzner](http://github.com/slinzner) - 核心开发者

[Florina Muntenescu](https://github.com/florina-muntenescu) - 核心开发者

[Sharif Salah](https://github.com/sharifsalah) - Technical Writer

[Doug Sigelbaum](https://github.com/DougSig) - Kotlin conversion

[Ben Weiss](https://github.com/keyboardsurfer) - Kotlin conversion

有关加入项目的更多信息，请参阅 [如何成为贡献者](https://github.com/googlesamples/android-architecture/blob/master/CONTRIBUTING.md) 和 [撰稿人指南](https：//github.com/googlesamples/android-architecture/wiki/Contributions)。
