# チェビシェフ横すべり脚 全方向移動ロボ（2サーボ, micro:bit）

**Chebyshev Side‑Slide Omni‑Walker (2 servos, micro:bit)** — サイバー100均ロボ / 八幡浜の三瀬医院

このリポジトリは、micro:bitで動作する「チェビシェフ横すべり脚」を用いた2サーボ全方向移動ロボの公開用データです。現時点では **.hex ファームウェア（ロボ本体・コントローラ）** を配布します。MakeCodeブロックやソースは今後追加予定です。

> 特徴
> - 2サーボのみで前進・後退・左右スライド・回転を実現
> - チェビシェフリンク + 横すべり脚（そろばん玉）機構
> - 100均素材で製作可能（竹串・割り箸・ストロー等）

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
  SHA256: `9329b6697c50991cde02c4b2c649c084ac5aa370c13378fc559b9fbc8e2f98a9`
- `controller_chebyshev_side_slide_2servo.hex`  
  SHA256: `6c60196de866dbd0a2cf246ec531b06b8d56f0dcb07e4248695366ae6750aca8`

（2025-09-19 時点）

---

## 使い方（書き込み手順）

1. **micro:bit をPCにUSB接続**（エクスプローラで `MICROBIT` ドライブとして認識されます）  
2. `firmware` フォルダ内の `.hex` を **ドラッグ&ドロップ** して書き込み  
   - ロボ本体用：`robot_chebyshev_side_slide_2servo.hex`  
   - コントローラ用：`controller_chebyshev_side_slide_2servo.hex`  
3. micro:bitのLEDが点滅し、転送完了後に自動リセットして起動します。

> **ヒント**: 2台の micro:bit を用意し、片方はロボ本体、もう片方はコントローラに書き込みます。

---

## ハードウェア構成（参考）

- **マイコン**: BBC micro:bit v1/v2（いずれか）×2（ロボ側・コントローラ側）  
- **サーボ**: SG90系 ×2（ロボ側）  
- **電源**: 単3/単4電池ボックス、またはUSB（必要電流に注意）  
- **機構材**: 100均の割り箸/竹串/ストロー、そろばん玉 等  
- **配線**: JST-PH系コネクタやピンヘッダ等（任意）

> 機構解説や組立ガイドは `docs/` に順次追加予定。

---

## 操作
- コントローラ micro:bit のボタン／ジェスチャで前後・左右・回転を操作（詳細は後日ドキュメント化）。
- 通信方式は micro:bit 標準の無線機能（MakeCode Radio）を使用。

---

## 既知の制約
- `.hex` はバイナリ配布のため、ブロック/ソースは同梱していません。  
- micro:bit の電源事情によりサーボ駆動が不安定な場合は外部電源や電圧降下対策を検討してください。

---

## ライセンス
- 本リポジトリ内 **ドキュメント／画像／自作コード**: MIT License（下記参照）  
- 同梱 `.hex` は Microsoft MakeCode / micro:bit ランタイムを含むため、その部分は各プロジェクトのライセンスに従います。

## クレジット
- Author: hitoshi katayama  
- Project: サイバー100均ロボ / 八幡浜の三瀬医院

---

## English (short)
This repo provides **micro:bit firmware (.hex)** for a 2‑servo omni‑directional walker using a **Chebyshev side‑slide leg** mechanism. Source (MakeCode blocks) will be added later.

### How to flash
1. Connect your micro:bit via USB (mounts as `MICROBIT`).  
2. Drag & drop the appropriate `.hex` from `firmware/` onto the drive.  
3. The board reboots and runs automatically.

### License
- Documents / images / original code: MIT.  
- Included `.hex` incorporate MakeCode/micro:bit runtime; please follow their licenses.
