
![](https://images.xiaozhuanlan.com/photo/2021/327790ad1afdb6b91bebdd423bc188a6.png)

# Smooth-Navigation

## 中文说明

提供安全可靠的 Navigation 操作，解决 GitHub 上开源的 "Navigation Add Hide 修改版" 普遍存在的 "popUpToInclusive 导致 Fragment 不符预期地加载" 等问题。

**使用方式：** 在 gradle 中添加 `com.kunminx.arch:smooth-navigation` 依赖，并将原有的 `androidx.navigation:navigation-fragment` 或修改版依赖 移除（否则在编译过程中会遭到原有依赖的覆盖）。

## Maven 依赖

- 以下 implementation 的命名，我们已从 `archi` 改为 `arch`，请注意修改，
- 鉴于 Jcenter 的关闭，我们已将仓库迁移至 Maven Central，请自行在根目录 build.gradle 添加 `mavenCentral()`。

```groovy
implementation 'com.kunminx.arch:smooth-navigation:3.9.0-beta1'
```

如果使用 kotlin 拓展，那么在上述的基础上，添加如下依赖即可：

```groovy
implementation('androidx.navigation:navigation-fragment-ktx:2.3.2') {
    exclude group: 'androidx.navigation', module: "navigation-fragment"
}
```

## English Guide

Provides safe and reliable Navigation operations, and solves the common problem of "popUpToInclusive causing Fragment to load unexpectedly" in the open source "Navigation Add Hide modified version" on GitHub.

**How to use:** Add `com.kunminx.arch:smooth-navigation` dependency in gradle, and remove the original `androidx.navigation:navigation-fragment` or modified version dependency (otherwise the original Dependent coverage).

## Maven dependency

- The following implementation is renamed. We have changed from `archi` to `arch`, so you should pay attention to the modification,
- Due to the closure of JCenter, we have migrated the warehouse to Maven Central, so you can add `mavenCentral()` in the root directory build.gradle.

```groovy
implementation 'com.kunminx.arch:smooth-navigation:3.9.0-beta1'
```

If you use kotlin extension, then on the basis of the above, add the following dependencies:

```groovy
implementation('androidx.navigation:navigation-fragment-ktx:2.3.2') {
    exclude group: 'androidx.navigation', module: "navigation-fragment"
}
```

## Thanks

感谢 @孙致远、@别睡太晚、@雅俗共赏 等小伙伴对 popUpToInclusive 以及嵌套 child 等场景下容错问题的反馈和测试 Demo 的提供。

## License

```
Copyright 2019-present KunMinX

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```