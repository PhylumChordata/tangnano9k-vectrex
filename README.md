# tangnano9k-vectrex
Tang Nano 9K top level module for vectrex

## 概要
- Tang Nano 9K用のトップレベルモジュールです．
- SourceForgeにあったDE10-lite用のソースを改変して作りました．

## コンパイル方法
- https://sourceforge.net/projects/darfpga/files/Software%20VHDL/vectrex/
にある"vhdl_vectrex_rev_0_2_2018_06_12.zip"を展開する．
- 展開してできた下記フォルダを，vectrex_project/src/に中身ごとコピーする．
 -- rtl_dar, rtl_jkent, rtl_mikej, rtl_pace
- ROMデータを用意する．
- Gawin EDAでvectrex_project.gprjをビルドする
-- ROMデータのファイルは，プロジェクトに適宜追加・削除して下さい．

## ROMデータについて
- 必要なROMデータは何らかの方法で入手して，オリジナルのパッケージに含まれるREADME.TXTに従ってvhdlファイルを作成して下さい．
-- romの名前，サイズに応じて，rtl_dar/vectrex.vhdの修正が必要です．

## 周辺回路について
- VGA出力，音声出力，キー入力は，hardware/tangnano9k-vectrex-peri-schematics.pdf の回路で動きました．
- たまたま手元にあった部品を使って作っただけなので，これが推奨回路というわけではありません．

## その他
- 27MHzのクロックを25MHzとして使っています．Tang NanoのPLLで25MHzのクロックが作れるかもしれないのでその方がいいかも．(私はPLLの使い方を知らないのと，IPを使いたくなかったので27MHzのクロックのまま使っています．)

