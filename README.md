# DOLOS 全时序 AU—音频曲线图集

无真假标签。信息点只是观察入口。未改 E0 / E0-T / Global+Soft-IIU / Event Observer。

## V2 发音动作与表达动作分层（当前）

本地完整交互页（含 WAV）在图集目录：

- V1：`index.html`
- V2：`v2/index.html`（四层独立纵轴：眉眼 AU04/07 · 嘴角 AU12/14 · 发音嘴部 AU10/20/25/26 · 声音）

**AU27 不在本 OpenFace 导出中，未伪造、未重跑视频。**

仓库里的 **`dolos_curve_lite_v2.zip`**（约 0.7 MB）：

- 同一 72 条观察样本
- 时间序列：AU04/07/12/14 与 AU10/20/25/26、confidence、success、log-RMS、F0、voicing
- IIU 起止、信息点、**已裁剪到 clip** 的词级时间
- V1 候选事件（阈值未改）+ **单独标记** 的发音通道事件（同一检测规则，计数不可与 V1 混合比较）
- **不含 WAV、不含原始 clip 名、不含真假标签**
- 不含 AU27

解压后看 `dolos_curve_lite_v2/README.md` 和 `index.csv`。匿名对照表只留本地，不进仓库。

V2 用法：看四层曲线 → 对照有声/停顿与 AU25 高峰附近的 AU12/14、AU04/07 → 同一人物多 clip。不要为找规律改事件阈值。不要把无法由发音解释的 AU 直接当异常。

## V1 轻量包（保留）

**`dolos_curve_lite.zip`**（约 1.6 MB）：72 样本 AU04/07/12/14、log-RMS、F0、IIU、信息点、V1 事件、`curve.svg`/`curve.png`。不含 WAV。

## 完整图集（含原始音频）

[Release v1.0](https://github.com/xiaochonglisi/dolos-av-curve-atlas/releases/tag/v1.0) 的 `DOLOS_AU_audio_curve_atlas.zip`（约 1.1 GB）。解压后双击 `打开.bat`（现默认打开 V2，顶栏仍有 V1）。
