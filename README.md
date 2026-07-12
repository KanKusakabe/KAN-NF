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

### 離散 × 連続 の対（失敗の事前検知＋反事実推奨で向く密度モデルは信号次第）
| プロジェクト | データ | 主な結果 |
|---|---|---|
| [Assembly101-NF](https://kankusakabe.github.io/Assembly101-NF/) | 玩具組立の離散手順（順序・トークン） | ミス検知 AUROC 0.80(自己回帰)/0.84(遷移カウント)・連続NFは0.63／反実 top-5 0.34 |
| [CaptainCook4D-NF](https://kankusakabe.github.io/CaptainCook4D-NF/) | 調理の連続実行ペース | held-out NLL Flow 1.43 vs ガウス混合 2.24／誤り検知 録画0.71・ステップ0.59／最小修正の反実 |

### 逆設計・空間 × 見守り（尤度を設計目的関数に／長期の“普通”）
| プロジェクト | データ | 主な結果 |
|---|---|---|
| [Layout-NF](https://kankusakabe.github.io/Layout-NF/) | TRUMANS 室内動作+占有グリッド | 配置検出 AUC0.92(未知シーン0.84)／家具の逆設計・反実 |
| [CASAS-NF](https://kankusakabe.github.io/CASAS-NF/) | CASAS 在宅センサ列 | 17ヶ月ドリフト／個人化は~300日で集団を超える |

### 空間動線 × 逆設計（一般の人の動線が漏らす「望まれた構造」を尤度で読む）
| プロジェクト | データ | 主な結果 |
|---|---|---|
| [DesirePath-NF](https://kankusakabe.github.io/DesirePath-NF/) | ETH/UCY 歩行者軌跡（けもの道） | LOSO NLL 0.85（位置ブラインド0.97・直進3.50）／desire×直進の偏差~40°＝構造条件が有効 |
| [CityFlow-NF](https://kankusakabe.github.io/CityFlow-NF/) | Gowalla チェックイン（Stockholm・立地） | 立地復元 AUC0.918（KDE0.926＝NFは超えず）／需要−供給ギャップで出店候補を逆設計 |
| [RouteDev-NF](https://kankusakabe.github.io/RouteDev-NF/) | Porto タクシー（ナビ逸脱） | 逸脱検知 AUC0.834／NF補正ルーターは F1 0.111→0.040 と悪化＝負の結果（IRLが要る） |

ページ本体は `docs/index.html`。リンクを増やす時はここを編集。
