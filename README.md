# 命理占卜 - 安卓原生版

## 项目概述

这是一个原生安卓应用，使用 WebView 包装网页版命理占卜应用。

### 特点

- ✅ 原生启动画面
- ✅ 全屏沉浸式体验
- ✅ 本地离线运行
- ✅ 所有功能完整保留
- ✅ 原生返回键支持

### 技术栈

- **开发语言**: Java
- **最低 SDK**: 21 (Android 5.0)
- **目标 SDK**: 34 (Android 14)
- **UI 框架**: WebView + Material Design

## 项目结构

```
mystical-android/
├── app/
│   └── src/main/
│       ├── java/com/mystical/divination/
│       │   ├── MainActivity.java      # 主界面
│       │   └── SplashActivity.java    # 启动画面
│       ├── res/
│       │   ├── layout/               # 布局文件
│       │   ├── values/               # 资源文件
│       │   └── drawable/             # 图形资源
│       ├── assets/www/               # 网页资源
│       └── AndroidManifest.xml
├── build.gradle
├── settings.gradle
└── gradle.properties
```

## 构建步骤

### 前置要求

1. **Android Studio** - https://developer.android.com/studio
2. **JDK 17** - Android Studio 自带
3. **Android SDK** - Android Studio 自带

### 构建 APK

1. 打开 Android Studio
2. 选择 `File` → `Open`
3. 选择 `mystical-android` 目录
4. 等待 Gradle 同步完成
5. 点击 `Build` → `Build Bundle(s) / APK(s)` → `Build APK(s)`
6. APK 文件在 `app/build/outputs/apk/debug/app-debug.apk`

### 更新网页内容

如果修改了网页代码：

```bash
# 1. 重新构建网页
cd mystical-pwa
npm run build

# 2. 复制到 Android assets
cp -r dist/* ../mystical-android/app/src/main/assets/www/

# 3. 在 Android Studio 中重新构建 APK
```

## 应用信息

| 项目 | 值 |
|------|-----|
| 应用名称 | 命理占卜 |
| 包名 | com.mystical.divination |
| 版本 | 1.0.0 |
| 最低 Android 版本 | 5.0 (API 21) |

## 功能列表

- 六爻占卜
- 八字简批
- 紫微斗数（本地版 + API版）
- 抽签问卦（观音灵签 + 诸葛神签）
- 塔罗牌占卜
- 星座运势
- 每日运势
- 六十四卦浏览
- 用户系统
- 历史记录

## 注意事项

1. **离线使用**: 所有功能支持离线使用
2. **塔罗牌图片**: 75张本地图片已打包在 assets 中
3. **隐私安全**: 所有计算在本地完成
4. **APK 大小**: 约 30-40 MB

## 常见问题

### Q: 如何修改应用图标？
A: 替换 `app/src/main/res/mipmap-*/ic_launcher.png` 文件。

### Q: 如何修改启动画面？
A: 编辑 `res/layout/activity_splash.xml` 文件。

### Q: 如何添加新功能？
A: 修改网页代码后，重新构建并复制到 assets 目录。

### Q: 构建失败怎么办？
A: 确保安装了 Android Studio 和 JDK 17，然后重新同步 Gradle。
