# チェビシェフ横すべり脚 全方向移動ロボ（2サーボ, micro:bit）

**Chebyshev Side-Slide Omni-Walker (2 servos, micro:bit)** — サイバー100均ロボ / 八幡浜の三瀬医院

このリポジトリは、micro:bitで動作する「チェビシェフ横すべり脚」を用いた2サーボ全方向移動ロボのファームウェアを公開するものです。  
機構や動画の詳細は [ProtoPedia作品ページ](https://protopedia.net/prototype/6763) にも掲載しています。

---

## 特徴
- **2つのSG90-HV連続回転サーボ**のみで、前後移動・左右スライド・その場回転が可能  
- **チェビシェフリンク機構＋横すべり脚（そろばん玉）**を組み合わせた独自の歩行方式  
- **100均素材**（竹箸・竹串・ストロー等）を用いて低コストで制作可能  

---

## 収録ファイル / Files

```
firmware/
 ├─ robot_chebyshev_side_slide_2servo.hex
 └─ controller_chebyshev_side_slide_2servo.hex
docs/
hardware/
```

### ハッシュ（検証用）
- `robot_chebyshev_side_slide_2servo.hex`  
  SHA256: 9329b6697c50991cde02c4b2c649c084ac5aa370c13378fc559b9fbc8e2f98a9
- `controller_chebyshev_side_slide_2servo.hex`  
  SHA256: 6c60196de866dbd0a2cf246ec531b06b8d56f0dcb07e4248695366ae6750aca8

（2025-09-19 時点）

---

## 使い方（書き込み手順）
1. micro:bit をPCにUSB接続（`MICROBIT` ドライブとして認識）  
2. `firmware` フォルダの `.hex` をドラッグ&ドロップして書き込み  
   - ロボ本体用：`robot_chebyshev_side_slide_2servo.hex`  
   - コントローラ用：`controller_chebyshev_side_slide_2servo.hex`  
3. 転送完了後、自動リセットして起動します。

---

## ハードウェア構成（参考）
- **マイコン**: BBC micro:bit v1/v2 ×2（ロボ側・コントローラ側）  
- **サーボ**: SG90-HV 連続回転サーボ ×2（ロボ側）  
- **電源**: 単4電池ボックス  
- **機構材**: 竹箸／竹串／ストロー／そろばん玉（100均素材中心）  
- **通信**: micro:bit 標準無線（MakeCode Radio）  

---

## 操作方法
- コントローラ側 micro:bit の **傾き（加速度センサー）** で全方向移動 

---

## 既知の制約
- `.hex` はバイナリ配布のため、ブロック/ソースは含まれていません（今後追加予定）  
- サーボ駆動は電源に依存するため、外部電源や昇圧回路で安定化が必要な場合があります  

---

## ライセンス
- 本リポジトリ内のドキュメント／画像／自作コード: MIT License  
- `.hex` 内のMicrosoft MakeCode / micro:bit ランタイムはそれぞれのライセンスに従います  

---

## クレジット
- Author: hitoshi katayama  
- Project: サイバー100均ロボ / 八幡浜の三瀬医院  
- 詳細紹介ページ: [ProtoPedia](https://protopedia.net/prototype/6763)

---

## English (short)

This repo provides **micro:bit firmware (.hex)** for a 2-servo omni-directional walker using a **Chebyshev side-slide leg** mechanism with **continuous rotation servos (SG90-HV)**.  

- 2 continuous rotation servos enable forward/backward, lateral slide, and in-place rotation.  
- Mechanism uses Chebyshev linkage + sliding legs (soroban beads).  
- Built with inexpensive 100-yen shop materials.  

For details and photos, see the [ProtoPedia page](https://protopedia.net/prototype/6763).
