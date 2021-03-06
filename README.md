# IoPLMaterials
Materials for the class "Implementation of Programming Languages" in Kyoto University.

## お知らせ

- 4月11日: [教科書3章 (ML1インタプリタ)](textbook/chap03-1.pdf)を一部修正しました．
- 4月5日: 2019年の講義資料ページを作りました．

## リンク集

- 実験3ホームページ: 未定
- 専門科目「プログラミング言語」ホームページ: https://github.com/aigarashi/PL-LectureNotes
  - の中の OCaml のページ（最低このくらいはわかってないとキツイ）: http://www.fos.kuis.kyoto-u.ac.jp/~igarashi/class/pl/03-ocaml.html
  - の中の OCaml で二分探索木を書くページ（これもわかってないとキツイ）: http://www.fos.kuis.kyoto-u.ac.jp/~igarashi/class/pl/04-bst-ocaml.html

## 講義に関する情報

- 講義をする人: 末永幸平（@ksuenaga, https://researchmap.jp/ksuenaga/）
- 講義が行われる時間: 月曜2限
- 講義が行われる場所: （多分）総合研究7号館講義室1
- Language used in the class: Japanese

## 講義予定

一部の資料と過去問は PandA で配布するので，PandA を見られる状態にしておくこと．
   
| 日付 | 内容 | 対応する教科書中の場所 |
|------|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4/8 | オリエンテーション，イントロダクション，OCaml入門 | [オリエンテーション資料](misc/orientation.md), [教科書1章](textbook/chap01.pdf), [教科書2章](textbook/chap02.pdf), [OCaml入門テキスト](textbook/mltext.pdf) |
| 4/15 | OCaml入門, ML1インタプリタ | [OCaml入門テキスト](textbook/mltext.pdf), [教科書3章 (ML1インタプリタ)](textbook/chap03-1.pdf)|
| 4/22 | | |
| 5/ 7 | | |
| 5/13 | | |
| 5/20 | | |
| 5/27 | | |
| 6/ 3 | 中間試験 | |
| 6/10 | | |
| 6/17 | | |
| 6/24 | | |
| 7/ 1 | | |
| 7/ 8 | | |
| 7/22 | | |
| ?/?? | | |

## OCaml の設定方法

OCaml のパッケージシステムである OPAM を用いてインストールするのが簡単である．
https://opam.ocaml.org/doc/Install.html を読んでインストールすること．
以下は簡便のために抜粋したものであるが，最新の情報ではないかもしれないので，できれば上記ページを読むこと．

- `sh <(curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh)`
  - `curl` 関係のエラーが出る場合は https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh のスクリプトをダウンロードして `sh install.sh` を実行．
  - 各自のパッケージ管理システム（Mac なら homebrew や macport，Linux なら yum や apt 等）を用いて opam をインストールしてもよい．
- `opam init` を実行
  - 途中設定ファイルに opam が書き込んでよいか聞かれる．全部 `y` にしておくと楽は楽である．
- ``eval `opam init` ``を実行
- ``eval `opam env` ``を実行
- `opam switch create 4.07.1`を実行
- ``eval `opam env` ``を実行

演習にはいくつかのパッケージが必要である．OPAM が入った状態であれば，以下のコマンドを実行することでこれらのパッケージを導入できる．

- `opam install menhir dune ounit`

便利情報がいくつかある．

- Emacs を使う人は tuareg-mode を使うとよい．`opam install tuareg` のあとに `opam user-setup install` を実行．
- emacs と vim では merlin https://ocaml.github.io/merlin/ が便利である．これがあるとエディタが IDE になる．`opam install merlin` のあとに `opam user-setup install` を実行．
  - Sublime-Text バージョンもベータ版として提供されている https://github.com/let-def/sublime-text-merlin
- VSCode で OCaml を使う方法がいくつかあるらしい．（調べた人は情報ください．）
  
