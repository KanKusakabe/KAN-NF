# KAN-NF — 人間データ × Normalizing Flow 統括

人間にまつわるデータに **条件付き Normalizing Flow** を適用した各プロジェクトを一覧する統括ページ。

**▶ 統括ページ（GitHub Pages）**: https://kankusakabe.github.io/KAN-NF/

条件付き Flow で `log p(行動 | 文脈)` を学習し、**尤度そのものを製品にする**。主な3つの使い方：
- **サプライズ = −log p**（異常・忘却・ミスの検知）
- **迷い = 予測エントロピー**（分岐・意思決定点の可視化）
- **反実生成**（本来どう動くべきかの生成）

## 収録プロジェクト

### NF × 人間データ 探索シリーズ（迷い＋反実の2レンズ）
| プロジェクト | データ | 主な結果 |
|---|---|---|
| [THÖR-MAGNI](https://kankusakabe.github.io/THOR-MAGNI/) | 屋内歩行者軌跡 | 屋内の迷い地図 ρ=0.77 |
| [Rehab-NF](https://kankusakabe.github.io/Rehab-NF/) | KIMORE リハビリ動作 | 脳卒中 AUC=0.69 / 腰痛0.52 |
| [MotionSim-NF](https://kankusakabe.github.io/MotionSim-NF/) | 音声合図→頭部（自作・介入） | 反応エントロピーの時間構造 |
| [GeoLife-NF](https://kankusakabe.github.io/GeoLife-NF/) | GPS移動（北京） | 迷い地図 ρ=0.57 |
| [ExtraSensory-NF](https://kankusakabe.github.io/ExtraSensory-NF/) | スマホ/時計センサ | 移行検出 AUC=0.73 |
| [eHMI](https://kankusakabe.github.io/eHMI/) | 車の合図→横断応答 | 横断の迷いは低ttcで最大 |
| [PMData-NF](https://kankusakabe.github.io/PMData-NF/) | Fitbit生活ログ | 典型日・睡眠規則性 |

### サプライズ = 忘却/ミス（配置・手順の異常検知）
| プロジェクト | データ | 主な結果 |
|---|---|---|
| [HD-EPIC-NF](https://kankusakabe.github.io/HD-EPIC-NF/) | 実キッチン3D配置+視線 | Flow>GMM (1.03<1.25) |
| [HoloAssist-NF](https://kankusakabe.github.io/HoloAssist-NF/) | 手順の逐次 | 介入予兆 AUC≈0.57 |
| [AI2-THOR-RoomR](https://kankusakabe.github.io/AI2-THOR-RoomR/) | シミュ配置 | 移動物検出 AUC=0.94 |

ページ本体は `docs/index.html`。リンクを増やす時はここを編集。
