Home Assistant Lovelace卡
Pascal配备了符合HACS标准的Lovelace仪表盘卡：custom:pascal-viewer-card.

用户安装流程：

在Home Assistant里安装HACS（如果还没安装的话）。
打开HACS，把这个GitHub仓库添加为带有类别的自定义仓库Dashboard.
安装Pascal 查看卡HACS。
刷新 Home Assistant 前端。
在Pascal里，连接Home Assistant，在场景中绑定设备，然后用Smart Home导出按钮下载/复制Lovelace卡配置。
在 Home Assistant 里，编辑仪表盘，添加一张手动卡，粘贴导出的配置。
这条路径仅限前端。它不需要对 Home Assistant 核心进行更改，custom_components、插件、脚本，或者写入 Home Assistant.storage.

开发者发布命令：

bun run build:lovelace
HACS丛被发射为dist/pascal-viewer-card.js， 和hacs.jsonHACS指向那个档案。

仓库架构
这是一个Turborepo单回收包，主要包含三个包裹：

editor-v2/
├── apps/
│   └── editor/          # Next.js application
├── packages/
│   ├── core/            # Schema definitions, state management, systems
│   └── viewer/          # 3D rendering components
