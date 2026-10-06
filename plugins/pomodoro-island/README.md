# 时钟岛 · pomodoro-island

灵动岛上的**番茄钟 + 随手倒计时**。界面照着 iOS 灵动岛做：蓝色矢量沙漏、沙子会漏、漏完会自己翻过来。

## 三层界面

**一级 · 收起态**（平时挂在屏幕顶上的胶囊）

```
⌛ 看书        71:36
```

蓝色沙漏 + 备注（倒计时显示）+ 白色大号时间。

**二级 · 展开态**（鼠标移到岛上）：沙漏变大，出现阶段标签，右侧「**蓝环 = 开始/暂停**」「**深灰圆 = 重置本段**」，标签和圆钮是一层层长出来的。

**三级 · 聚光卡**（点击岛体）：一张**白色控制台**，顶部两个页签 **番茄钟 / 倒计时**。

## 功能

- **番茄钟**：专注 → 短休息 → 长休息循环，可设每几个番茄进一次长休；**今日完成数 / 今日专注时长 / 本轮进度**三张彩色统计卡 + 最近记录
- **随手倒计时**：「3 分钟后去煮面」这种；时长随意、可写备注，备注直接显示在岛上
- **会动的沙漏**：贝塞尔曲线玻璃 + 上罩漏斗形塌陷 + 下罩锥形沙堆 + 16 颗飘落沙粒（重力加速、翻滚、左右飘）+ 漏完翻转
- 所有调时间的地方都是**滑块**，± 号做单步微调
- 今日统计写入插件目录的 `stats.json`，重启不丢，跨天自动清零
- 结束响系统提示音 + 岛上弹提醒

## 截图

> 客户端不渲染图片，点下面链接看图：

- [一级 · 收起态](https://github.com/hitikem/clock-island/blob/main/screenshots/island.png)
- [二级 · 悬停展开](https://github.com/hitikem/clock-island/blob/main/screenshots/island-expanded.png)
- [三级 · 倒计时卡片](https://github.com/hitikem/clock-island/blob/main/screenshots/card-countdown.png)
- [三级 · 番茄钟卡片](https://github.com/hitikem/clock-island/blob/main/screenshots/card-pomodoro.png)

## 安装

把 `pomodoro-island-1.0.0.lwp` 拖进 WinIsland 的 `plugins\` 目录，重启 WinIsland 会自动安装并删除包。

装好后在 **设置 → 插件 → 番茄小岛** 里调设置。**如果岛上没显示**，把「显示优先级」调到 100 以上（宿主内置媒体模块是 200）。

## 权限与数据

- **不联网**、不采集、不上传任何数据
- 只读写 WinIsland 的插件设置（键自动带 `pomodoro-island.` 前缀）和自己插件目录下的 `stats.json`
- **不需要管理员权限**

## 测试环境

- WinIsland：v1.1.2（宿主 SDK 2.3.1.0，`api_version` 2）
- 系统：Windows 11
- 分辨率：1366×768

## 源码仓库

<https://github.com/hitikem/clock-island>

## 许可与免责

MIT。个人兴趣作品，按「现状」提供，**使用风险自负**；番茄钟是效率辅助工具，不能替代医疗、安全等场景下的专业计时设备。

## 更新记录

- **1.0.0**（2026-10-07）：首个版本 —— 番茄钟、随手倒计时、会动的沙漏、白色控制台、滑块设置、今日统计持久化
