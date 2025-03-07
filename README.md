# 月经月历 Android 小组件

一个简单而强大的月经月历 Android 小组件，帮助女生跟踪月经周期并理解体内激素变化的影响。但是！这是一个计划！还没有做好。

## 功能

- **桌面小组件**：直接在主屏幕上显示28天月经周期视图
- **个性化定制**：用户可以设置周期起始日期，应用将自动计算28天周期
- **激素状态追踪**：根据周期日自动识别体内主导激素状态
- **情绪和体验记录**：记录每天的情绪和身体感受
- **数据洞察**：帮助用户理解激素变化对自身的影响

### 爆金助力
![wechat-pay](https://github.com/user-attachments/assets/83feb6cd-20ba-466e-a21b-48f7bb9a1aac)

## 技术实现

本应用使用以下技术栈：

- **Android Jetpack**：
  - Room 数据库：本地存储用户数据
  - ViewModel 和 LiveData：管理UI相关数据
  - Jetpack Compose：构建现代化UI (可选)
  - App Widget：实现桌面小组件功能
- **Kotlin**：主要开发语言
- **Material Design**：现代化UI设计
- **WorkManager**：管理后台任务，定时更新小组件

## 关于我

An independent philosopher or somebody who don't like shit. Sometimes I make tools for girls to have fun.無駄に生きることを誇りに思っている
个人网站：https://storied-donut-86f070.netlify.app/

## 数据模型

本应用使用简单的数据模型来表示月经周期：

- **周期日(CycleDay)**：表示28天周期中的某一天
  - 日期
  - 周期日号(1-28)
  - 激素状态
  - 情绪记录
  - 症状记录

## 项目结构

```
app/
├── src/main/
│   ├── java/com/yourpackage/
│   │   ├── data/           # 数据层
│   │   │   ├── AppDatabase.java
│   │   │   └── CycleDayDao.java
│   │   ├── model/          # 数据模型
│   │   │   └── CycleDay.java
│   │   ├── repository/     # 存储库
│   │   │   └── CycleRepository.java
│   │   ├── ui/             # UI层
│   │   │   ├── MainActivity.java
│   │   │   └── SettingsActivity.java
│   │   ├── util/           # 工具类
│   │   │   └── DateUtils.java
│   │   ├── viewmodel/      # ViewModel
│   │   │   └── MainViewModel.java
│   │   └── widget/         # 小组件
│   │       └── CycleCalendarWidget.java
│   ├── res/
│   │   ├── layout/         # 布局文件
│   │   │   ├── activity_main.xml
│   │   │   └── cycle_calendar_widget.xml
│   │   └── xml/
│   │       └── cycle_calendar_widget_info.xml
│   └── AndroidManifest.xml
└── build.gradle
```

## 安装和使用

1. 从Release页面下载最新版APK或从Google Play等应用商城安装（正在开发中）
2. 长按主屏幕空白处，选择"小组件"
3. 找到"月经月历"小组件，拖到主屏幕
4. 首次使用时，请设置您的周期起始日期

## 贡献

欢迎提交Issue和Pull Request！

## 许可证

本项目采用MIT开源协议。
