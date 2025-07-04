# Regex Rule Transformers

A system to transform some input string using a list of rules that you define.

The rules use regular expressions, and also some lookback functionality.

The transformation is performed in a single pass.

## How to use

You can use this repo in the following ways:

* The [online version](https://kotlinguistics.github.io/IPA-Transcribers)
* ~~Desktop app~~ TODO: replace broken JavaFX with Jetpack Compose
* local webpage
* as a library in your JVM/Android project

<details>
  <summary><b>As a local webpage</b></summary>

To build it:

```shell script
./gradlew jsBrowserWebpack
./update-site.sh # or manually copy the files specified in that script
```

then open `./docs/index.html` in your browser.

</details>

<details>
  <summary> <b><strike>As a Java desktop app</strike></b></summary>

to build it:

```shell script
./gradlew shadowJar
```

~~to run it:~~ (currently broken)

```shell script
java -jar build/libs/IPA-transcribers-0.3-all.jar
```

</details>

<details>
  <summary><b>As a library in a Gradle/Maven project</b></summary>


First, add the jitpack repository to your repositories if you haven't already:

`gradle`
``` gradle
allprojects {
    repositories {
        maven { url 'https://jitpack.io' }
    }
}
```

`maven`
``` xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
```

Then add this library to your project:

`gradle`
``` gradle
dependencies {
    implementation 'com.github.medavox:IPA-Transcribers:v0.3'
}
```

`maven`
``` xml
<dependency>
    <groupId>com.github.medavox</groupId>
    <artifactId>IPA-Transcribers</artifactId>
    <version>v0.3</version>
</dependency>
```
</details>

The bulk of this project lives in [this directory](./src/commonMain/kotlin/com/github/medavox/ipa_transcribers).
