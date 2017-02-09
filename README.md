# Recompiled pinyin4j


This is a recompiled version of **Li Min**'s **pinyin4j**(v2.5.0) released on [SourceForge](https://sourceforge.net/projects/pinyin4j/).

How to recompile?
+ Create a new Java project and copy sources `pinyin4j-2.5.0.zip/src/net/sourceforge/pinyin4j/` (Ignore `pinyin4j-2.5.0.zip/src/demo/`, `pinyin4j-2.5.0.zip/src/testcase/`).
+ Copy database text files from `pinyin4j-2.5.0.zip/lib/pinyin4j-2.5.0.jar/pinyindb/`.
+ Download dependency library `sparta-src-20031101.zip` [here](http://sparta-xml.sourceforge.net/).
+ Copy sources `sparta-src-20031101.zip/sparta/java/com/hp/hpl/sparta/` (Ignore `sparta-src-20031101.zip/sparta/java/com/hp/hpl/thermopylae/`, `sparta-src-20031101.zip/sparta/java/com/hp/hpl/sparta/test`; remove unuseful files).
+ Export JAR files.

Get it: [pinyin4j-recompiled-2.5.0.2.jar](out/pinyin4j-recompiled-2.5.0.2.jar)

How to use in Android project?
+ Copy `pinyin4j-recompiled-2.5.0.2.jar` to `libs` folder of your project.
```
dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
}
```
+ if
```
buildTypes {
    release {
        minifyEnabled true
        proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
    }
}
```
then `proguard-rules.pro`
```
# pinyin4
-keep class net.sourceforge.pinyin4j.** { *;}
```


*Copyright &#169; 2017 By_syk. All rights reserved.*