# 音乐播放器（APlayer）

> 迁移自：[音乐播放器](https://docs.tangly1024.com/article/notion-next-plugin-music-player)  
> 实现：`components/Player.js`、`conf/widget.config.js`

全站挂件，**所有主题通用**（含 Proxio）。

## 快速开启

```bash
NEXT_PUBLIC_MUSIC_PLAYER=true
NEXT_PUBLIC_MUSIC_PLAYER_AUTO_PLAY=true
NEXT_PUBLIC_MUSIC_PLAYER_VISIBLE=false   # 隐藏控制条 ≈ 背景音乐
```

或在 Notion Config 表配置同名键。

## 常用配置

| 配置键 | 说明 |
| --- | --- |
| `MUSIC_PLAYER_AUTO_PLAY` | 自动播放（移动端常被浏览器拦截） |
| `MUSIC_PLAYER_VISIBLE` | `false` 时隐藏左下角 UI |
| `MUSIC_PLAYER_AUDIO_LIST` | 自定义曲目 JSON 数组（`name`/`artist`/`url`/`cover`） |
| `MUSIC_PLAYER_METING` | `true` 时用 MetingJS 拉网易云等歌单 |
| `MUSIC_PLAYER_METING_SERVER` | `netease` / `tencent` 等 |
| `MUSIC_PLAYER_METING_ID` | 歌单 ID |
| `MUSIC_PLAYER_ORDER` | `list` 顺序 / `random` 随机 |

自定义列表示例见 `conf/widget.config.js`。更多参数见 [APlayer 文档](https://aplayer.js.org/#/zh-Hans/)。

## Proxio 欢迎层

开启 `PROXIO_WELCOME_COVER_ENABLE` 时，用户点击进站后再播放，更容易通过浏览器自动播放策略。

## 原文链接

https://docs.tangly1024.com/article/notion-next-plugin-music-player
