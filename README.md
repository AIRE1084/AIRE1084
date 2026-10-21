# 你好，我是 AIRE1084

软件工程专业在读。做校园工具与本地自动化 —— 把每天要重复点十几次的流程，压成一次点击。

## 在做的事

**[新理Lite](https://github.com/AIRE1084/xllite-HarmonyOS)** — 面向在校学生的民间校园服务 App。同一套学校接口契约，两套互不相干的实现：

| 分支 | 名称 | 技术栈 | 平台 |
| --- | --- | --- | --- |
| `main` | 新理Lite | Flutter / Dart | Android、iOS |
| `harmony` | 掌上新理工 · HarmonyOS | ArkTS / ArkUI | HarmonyOS 6.1+（最低 API 23，按 API 26 编译） |

承载的高频查询：课表 · 成绩 · 考试安排 · 校园卡余额与流水 · 宿舍电费。

鸿蒙侧接了 Flutter 层拿不到的系统能力：实况窗倒计时（`TIMER` 场景进胶囊、锁屏与通知中心）、小艺意图分发、API 26 原生沉浸材质（低版本回落 `backgroundEffect`）、`reminderAgentManager` 托管课程提醒、`CampusFormAbility` 桌面服务卡片。跨版本能力一律运行时判版本后动态导入，不进低版本调用路径。

两边共同守的几条线：

- CAS 凭据只落在本机安全存储，不写日志、不上传第三方
- 网络异常时回落到最近一次成功缓存，不假装成功
- 推 `v*` tag 触发 GitHub Actions，产出 release APK 与未签名 IPA（供自签工具重签安装）

> 民间开发版本，不代表任何学校官方应用，也未上架应用市场。

## 技术栈

`Dart` `Flutter` `ArkTS` `ArkUI` `TypeScript` `Node.js` `Python` `PowerShell` `GitHub Actions`

## 工作方式

先把行为验证清楚，再写代码。能复现的才算修好；说不清触发条件的，一律按没修处理。

## 找得到我

- 代码：下方 Pin 住的仓库
- 问题与建议：直接开 Issue
