# presents.Vision.Qwen3VL · Qwen3-VL视觉分析

基于 Qwen3-VL-4B 的本地视觉分析引擎，支持思考模式（可开关）。作为 `Alife.Function.Vision` 的本地实现接入，其他插件（视频理解、B站抽帧识图等）可直接调用。

依赖 `Alife.Function.AIModelUtility` 与 `Alife.Function.Vision`。模型权重不随插件分发，首次使用由客户端按配置下载。

## 安装

解压后目录名必须与插件 id 一致（`presents.Vision.Qwen3VL`），放到 Alife 的 `Storage/Plugins/` 下，重启后由客户端自行编译加载。

Python 依赖见 `manifest.json` 的 `Environments.pip`（torch、torchvision、transformers、bitsandbytes、accelerate、sentencepiece、tiktoken、Pillow、qwen-vl-utils、huggingface-hub、torchcodec）。

## 版本

当前版本 **5.1.0**，发布包见 [Releases](https://github.com/presents0721/presents.Vision.Qwen3VL/releases)。

插件大版本与 Alife 大版本对应：5.x 只给 Alife 5.0.0+ 用，4.x 请勿安装或更新到 5.x（两条线功能一致，底层接口按版本适配）。

## 源码

仓库结构即插件目录结构：`manifest.json` + `*.cs` + `Resources/`。运行时产生的 `out/`、`state.json` 等不进仓库（见 `.gitignore`）。
