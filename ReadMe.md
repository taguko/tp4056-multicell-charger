# TP4056 Multicell Charger

USB Type-C入力で小容量の多セル LiPo / Li-ion バッテリーを充電するための充電器です。

## 特徴

- USB Type-C入力
- 2S / 3Sセル対応
- 各セル独立CC/CV充電
- TP4056ベース
- 絶縁DC/DCコンバータ採用
- バランサ回路不要

## コンセプト

一般的な多セル充電器は、パック全体を充電しながらセル間の電圧差をバランサで調整します。

本プロジェクトでは、各セルを独立した充電回路で直接充電することで、セル電圧を揃える方式を採用しています。

## ディレクトリ構成

```
.
├── tp4056-multicell-charger.kicad_sch
├── tp4056-multicell-charger.kicad_pcb
├── Charger_Module.kicad_sym
├── DCDC.kicad_sym
├── Charger_Module.pretty/
└── DCDC.pretty/
```

## 使用上の注意

- LiPo / Li-ionバッテリー専用です。
- 破損したバッテリーには使用しないでください。
- 充電中は目の届く場所で使用してください。
- 本プロジェクトの使用によって生じた損害について作者は責任を負いません。

## ライセンス

MIT License
