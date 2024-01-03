# Webview

The Java port of the [webview project](https://github.com/webview/webview). It uses JNA under the hood to interface with the webview library, auto extrating the required dll/dylib/so libraries for your current system.

<div align="center">
    <img alt="browser" src="demo.png" width="50%" />
    <br />
    <br />
</div>

## Examples

[Example](https://github.com/webview/webview_java/blob/main/core/src/test/java/com/example/webview_java/Example.java)  
[Bridge Example](https://github.com/webview/webview_java/blob/main/bridge/src/test/java/com/example/webview_java/BridgeExample.java)

### macOS

macOS requires that all UI code be executed from the first thread, which means you will need to launch Java with `-XstartOnFirstThread`. This also means that the Webview AWT helper will NOT work at all.

## Getting the code

Replace `_VERSION` with the latest version or commit in this repo. If you want the Bridge bindings you'll need both `core` and `bridge`.

<details>
  <summary>Maven</summary>
  
```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>

<dependency>
    <groupId>com.github.webview.webview_java</groupId>
    <artifactId>core</artifactId>
    <version>_VERSION</version>
</dependency>
```
</details>

<details>
<summary>Gradle</summary>

```gradle
allprojects {
  repositories {
    maven { url 'https://jitpack.io' }
  }
}

dependencies {
  implementation 'co.casterlabs:Commons.core:_VERSION'
}
```

</details>

<details>
  <summary>SBT</summary>

```sbt
resolvers += "jitpack" at "https://jitpack.io"

libraryDependencies += "com.github.webview.webview_java" % "core" % "\_VERSION"
```

</details>

<details>
<summary>Leiningen</summary>

```lein
:repositories [["jitpack" "https://jitpack.io"]]

:dependencies [[com.github.webview.webview_java/core "_VERSION"]]
```

</details>
