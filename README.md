# 🤖 Astrbot Sowing discord rebuild 模块 - 搬史插件（非原作重构版）

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Python Version](https://img.shields.io/badge/Python-3.10.14%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen)](CONTRIBUTING.md)
[![Contributors](https://img.shields.io/github/contributors/anka-afk/astrbot_plugin_meme_manager?color=green)](https://github.com/anka-afk/astrbot_plugin_meme_manager/graphs/contributors)
[![Last Commit](https://img.shields.io/github/last-commit/anka-afk/astrbot_plugin_meme_manager)](https://github.com/anka-afk/astrbot_plugin_meme_manager/commits/main)

</div>

<div align="center">

[![Moe Counter](https://count.getloli.com/get/@GalChat?theme=moebooru)](https://github.com/anka-afk/astrbot_sowing_discord)

</div>

让 AI 学会搬史, 搬史进入新时代! 全自动搬史!

## ✨ 功能

- 🚀 自动从指定的群聊转发聊天记录(史)到其他指定的群聊
- ⚡ 即时转发，无需等待评价
- 🎯 支持自定义消息类型过滤（文本、图片、视频、转发消息）

## 🛠️ 使用方法

1. 在配置中设置 `banshi_group_list` 为消息来源群号
2. 设置 `banshi_target_list` 为目标群号（留空则转发到所有群）
3. bot 开始全自动搬史!

## ❓ 常见问题

1. **Q: 为什么我的 bot 没有自动搬史?**

   - A: 请检查以下项目:
     - 1. 确认已在 `banshi_group_list` 中正确配置了来源群号
     - 2. 确认 bot 在来源群和目标群中都有正常权限
     - 3. 查看控制台日志确认是否有错误信息

## ⚙️ 配置说明

插件配置项包括：

- `banshi_interval`: 搬史间隔, 单位: 秒（兼容项，实际冷却由时间段动态决定）
- `banshi_cache_seconds`: 消息缓存时间限制, 也是转发前检查历史消息的时间窗口 (秒)
- `banshi_cooldown_day_seconds`: 动态冷却-白天冷却秒数（默认 600）
- `banshi_cooldown_night_seconds`: 动态冷却-夜间冷却秒数（默认 3600）
- `banshi_cooldown_day_start`: 动态冷却-白天时段起始时间（HH:MM，默认 09:00）
- `banshi_cooldown_night_start`: 动态冷却-夜间时段起始时间（HH:MM，默认 01:00）
- `banshi_group_list`: 史的来源群列表（**必须手动配置群号**，默认为空）
- `banshi_target_list`: 白名单, 史的目标列表, 可以填写多个群或用户, 默认空白即全部群
- `block_source_messages`: 开启后将屏蔽 banshi_group_list 中的群消息
- `allowed_message_types`: 允许转发的消息类型，可选: text(文本), image(图片), video(视频), forward(聊天记录/合并转发)

## 👥 贡献指南

欢迎通过以下方式参与项目：

- 🐛 提交 Issue 报告问题
- 💡 提出新功能建议
- 🔧 提交 Pull Request 改进代码

## 📄 许可证

本项目基于 MIT 许可证开源。
