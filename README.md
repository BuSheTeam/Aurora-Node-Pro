# Aurora Node Pro
![](https://img.shields.io/badge/Android-5.0%20--%2012-blue.svg?style=flat)
![](https://img.shields.io/badge/arch-armeabi--v7a%20%7C%20arm64--v8a%20%7C%20x86%20%7C%20x86__64-blue.svg?style=flat)  

欢迎使用 Aurora Node Pro，这是一个原生实现的 Node 运行环境。  
此版本是 [NodeAurora](https://github.com/BuShe-LLC/NodeAurora) 的 **Pro** 版本，相比 NodeAurora，此版本包含以下特性：
* 🌟 不再需要动态原生支持库
* 👀 对 Android 6.0 以下有更好的兼容性
* 🌍 去除了 Node 自有的国际化支持
* 🚀 大幅优化了运行效率
* 🐱 支持 Node 与 Java 之间的交互
## 用法
如同 *NodeAurora* 一样，在你的应用程序中，你需要先初始化 Aurora Node Pro 实例，我们建议在 Application 中进行初始化：
```java
// 初始化 Aurora Node Pro 实例
// 我们强烈建议在 Application 中的 onCreate() 方法中初始化
// 这是个 static 方法，只需要在应用程序启动时调用一次
// 你可以在初始化之后使用 Aurora.getNodeVersion() 获取当前引入的 Node.js 的版本
Aurora.initialize();
```
在完成初始化之后，你可以在任意你想要创建 Aurora Node 运行环境的地方使用 `Aurora.Builder()` 构造运行环境：
```java
new Aurora.Builder(Context context).build();
```
Builder 接受以下方法（参数）：

| Method                                  | Description                       |
|-----------------------------------------|-----------------------------------|
| setNodeAppDictionary(String)            | 设置 Node 的工作目录，可接受参数 String: 绝对路径  |
| setNodePackageManagerSupported(Boolean) | 是否选择支持 Node Package Manager (NPM) |
| build()                                 | 立即构造 Aurora Node 环境               |



## 致谢与协作者
### 协作者
东灯 Lampese <<me@lampese.com>>
### 致谢
[项目早期测试人员] Dexer Matters <<dexermatters@gmail.com>>
