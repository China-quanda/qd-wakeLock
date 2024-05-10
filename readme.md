# qd-wakeLock 开发文档

## WakeLock是什么
WakeLock是Android框架层提供的一套机制，应用使用该机制可以达到控制Android设备状态的目的。这里的设备状态主要指屏幕的打开关闭，cpu的保持运行。简单的理解WakeLock是让系统保持"清醒"的一种手段

## WakeLock作用
当手机灭屏状态下保持一段时间后，系统会进入休眠，一些后台运行的任务就可能得不到正常执行，比如网络下载中断，后台播放音乐暂停等。WakeLock正是为了解决这类问题，应用只要申请了WakeLock，那么在释放WakeLock之前，系统不会进入休眠，即使在灭屏的状态下，应用要执行的任务依旧不会被系统打断。

## 功能

- 开启WakeLock锁。
- 释放WakeLock锁。
- 查询是否打开WakeLock锁。

## 安装

请将此插件的代码包括在您的项目中，并确保所有依赖项正确导入。

## 如何使用

### 在 script 中引入

```
import { acquireWakeLock, releaseWakeLock, isOpenWakeLock } from '@/uni_modules/qd-wakeLock';
```


### 查询是否打开WakeLock锁

```
console.log(isOpenWakeLock()); // true || false

```

### 开启WakeLock锁

```
acquireWakeLock()
```

### 释放WakeLock锁

```
releaseWakeLock()
```

## 注意事项

请确保您的应用遵守相关平台的政策和指南。

## 贡献

欢迎对此插件提出改进建议或提交问题报告。



