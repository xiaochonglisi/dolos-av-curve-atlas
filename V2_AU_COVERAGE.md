# V2 AU 数据覆盖

不修改 V1 JSON。未重跑 OpenFace。未伪造缺失通道。

- clips: 1479 · 观察集 72
- OpenFace AU*_r 并集: AU01, AU02, AU04, AU05, AU06, AU07, AU09, AU10, AU12, AU14, AU15, AU17, AU20, AU23, AU25, AU26, AU45
- 请求：眉眼 AU04/07；嘴角 AU12/14；发音 AU10/20/25/26/27
- **AU27 不存在**（1479/1479 缺列）。未伪造，未重处理视频。
- 其余请求通道 1479/1479 均有 `AUxx_r`
- 平均 OpenFace confidence ≈ 0.952；低置信显示阈值 0.5
- 词级时间：本批 V1 词戳均已落在 clip 内（裁剪 0 / 丢弃 0）；若越界会裁剪并标 `clipped_to_clip`

V1 事件阈值未改。V2 对 AU10/20/25/26 单独生成 `au_change_articulatory`，规则 `|dAU|≥median+2.5×1.4826×MAD`、最短 80ms，**不可与 V1 事件计数混合比较**。
