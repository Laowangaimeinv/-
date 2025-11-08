# Neat
Functional minimalistic Unit Frames for the modern Minecrafter

## Modified by 隔壁老王 (Neighbor Laowang)
This is a modified version with Pixelmon support features.

### New Features / 新增功能
- **Pixelmon Pokemon Stats Display / 宝可梦数值显示**: Display Pokemon IV/EV values above health bars / 在生命条上方显示宝可梦个体值/努力值
  - Server-side data synchronization / 服务端数据同步
  - Client-side caching system (30s expiration) / 客户端缓存系统（30秒过期）
  - Color-coded Chinese display / 彩色中文显示
  - Per-player tick counter for multiplayer support / 多玩家独立tick计数器
  - Displays IVs and EVs with attribute names / 显示带属性名称的个体值和努力值
- **Separate compilation / 分离编译**: Generate server-only, client-only, and universal JAR files / 生成服务端专用、客户端专用和通用JAR文件
- **Bilingual code comments / 双语代码注释**: All core code includes Chinese and English comments / 所有核心代码包含中英文注释
- **Configuration localization / 配置汉化**: Complete Chinese translation for all config options / 所有配置项的完整中文翻译

## Support plan
Due to Mojangs fast version changing, it's impossible to support all versions at the same time.
Because of this Neat will from now on only support two Minecraft Versions simultaneously, a Long-Term-Support (LTS) version and the newest available version.
I will choose the LTS version myself based on what feels like the currently most popular version.
The two supported versions are currently:
- LTS: 1.21.1
- Newest: 1.21.10 (currently wip)

## Release Process
Neat's release process is mostly automated. Here's the steps:

1. Pull master so you're up to date, make sure everything is committed
2. Run `git tag -a release-<mc_version>-<build_number>`. If you don't know or remember what those are, look at `gradle.properties`
3. In the editor that pops up, write the changelog
4. In `gradle.properties`, increment the build_number by one for the next version. Commit this.
5. Push master and the release tag: `git push origin master release-<mc_version>-<build_number>`
6. Shortly after, the mod should be automatically uploaded to GitHub's release tab, Modrinth, and CurseForge.

## Signing
Releases are signed with the Violet Moon signing key, see [this
page](https://github.com/VazkiiMods/.github/blob/main/security/README.md) for information
about how to verify the artifacts.
