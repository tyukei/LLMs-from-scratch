# 大規模言語モデルをスクラッチで作ろう
\[ [英語版](README.md) | [日本語] \]

このリポジトリは、GPTのようなLLMを開発・事前学習・ファインチューニングするコードを含んでおり、書籍『[つくりながら学ぶ！LLM 自作入門 ](https://amzn.asia/d/1BufK0J)』の公式コードリポジトリです。

<br>
<br>

<a href="https://amzn.to/4fqvn0D"><img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/cover.jpg?123" width="250px"></a>

<br>

[つくりながら学ぶ！LLM 自作入門 ](https://amzn.asia/d/1BufK0J) では、大規模言語モデル（LLM）がどのように動作するのかを、コードをゼロから段階的に書きながら内側から理解できるように解説します。書籍内では、テキストや図、例を用いて各ステージをわかりやすく説明しながら、独自LLMを作る方法を案内しています。

本書で紹介している教育向けの小規模モデルを作るための方法は、ChatGPTのベースとなるような大規模ファウンデーションモデルの開発手順を縮小したものと同じ手順を採用しています。さらに、この書籍では大規模事前学習済みモデルを読み込み、ファインチューニングするためのコードも含まれています。

- 公式[ソースコードリポジトリ](https://github.com/rasbt/LLMs-from-scratch)  
- [出版社サイト（Manning）での書籍紹介ページ](http://mng.bz/orYv)  
- [Amazon.comの書籍紹介ページ](https://amzn.asia/d/1BufK0J) 
- ISBN 9781633437166

<a href="http://mng.bz/orYv#reviews"><img src="https://sebastianraschka.com//images/LLMs-from-scratch-images/other/reviews.png" width="220px"></a>

<br>
<br>

このリポジトリをダウンロードしたい場合は、[Download ZIP](https://github.com/rasbt/LLMs-from-scratch/archive/refs/heads/main.zip) ボタンをクリックするか、下記のようにターミナルでコマンドを実行してください。

```bash
git clone --depth 1 https://github.com/rasbt/LLMs-from-scratch.git
```

<br>

（もしManningのサイトからコードバンドルをダウンロードされた場合でも、最新の更新を確認したい場合は、公式コードリポジトリ https://github.com/rasbt/LLMs-from-scratch を確認することをおすすめします。）

<br>
<br>

# 目次

この `README.md` ファイルはMarkdown (`.md`) 形式で書かれています。もしManningのサイトからコードをダウンロードし、ローカル環境で閲覧している場合、Markdownエディタやプレビュー機能を使用すると読みやすくなります。まだMarkdownビューアを導入していない場合は、[MarkText](https://www.marktext.cc) などの無料ツールもよいでしょう。

あるいは、ブラウザ上でMarkdownが自動的にレンダリングされるGitHub上で [https://github.com/rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch) を閲覧していただく方法も便利です。

<br>
<br>
<!--  -->

> **ヒント:**
> PythonやPythonのパッケージのインストール、および実行環境のセットアップについてのアドバイスが必要な場合は、[setup](setup) ディレクトリ内にある [README.md](setup/README.md) ファイルを参照してください。

<br>
<br>

[![Code tests Linux](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-linux-uv.yml/badge.svg)](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-linux-uv.yml)
[![Code tests Windows](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-windows-uv-pip.yml/badge.svg)](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-windows-uv-pip.yml)
[![Code tests macOS](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-macos-uv.yml/badge.svg)](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-macos-uv.yml)

<br>

| 章・タイトル                                                   | 主なコード（クイックアクセス用）                                                                                                                                                                                                       | すべてのコード＋補足                                       |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [セットアップ推奨事項](setup)                                  | -                                                                                                                                                                                                                                  | -                                                       |
| 第1章: LLMを理解する                                          | コードなし                                                                                                                                                                                                                             | -                                                       |
| 第2章: テキストデータの扱い方                                 | - [ch02_ja.ipynb](ch02/01_main-chapter-code/ch02_ja.ipynb)<br/>- [dataloader.ipynb](ch02/01_main-chapter-code/dataloader.ipynb)（まとめ）<br/>- [exercise-solutions.ipynb](ch02/01_main-chapter-code/exercise-solutions.ipynb)                     | [./ch02](./ch02)                                        |
| 第3章: アテンションメカニズムをコーディングする                | - [ch03.ipynb](ch03/01_main-chapter-code/ch03.ipynb)<br/>- [multihead-attention.ipynb](ch03/01_main-chapter-code/multihead-attention.ipynb)（まとめ） <br/>- [exercise-solutions.ipynb](ch03/01_main-chapter-code/exercise-solutions.ipynb) | [./ch03](./ch03)                                        |
| 第4章: GPTモデルをスクラッチで実装する                        | - [ch04.ipynb](ch04/01_main-chapter-code/ch04.ipynb)<br/>- [gpt.py](ch04/01_main-chapter-code/gpt.py)（まとめ）<br/>- [exercise-solutions.ipynb](ch04/01_main-chapter-code/exercise-solutions.ipynb)                                   | [./ch04](./ch04)                                        |
| 第5章: ラベルなしデータでの事前学習                           | - [ch05.ipynb](ch05/01_main-chapter-code/ch05.ipynb)<br/>- [gpt_train.py](ch05/01_main-chapter-code/gpt_train.py)（まとめ）<br/>- [gpt_generate.py](ch05/01_main-chapter-code/gpt_generate.py)（まとめ）<br/>- [exercise-solutions.ipynb](ch05/01_main-chapter-code/exercise-solutions.ipynb) | [./ch05](./ch05)                                        |
| 第6章: テキスト分類へのファインチューニング                    | - [ch06.ipynb](ch06/01_main-chapter-code/ch06.ipynb) <br/>- [gpt_class_finetune.py](ch06/01_main-chapter-code/gpt_class_finetune.py) <br/>- [exercise-solutions.ipynb](ch06/01_main-chapter-code/exercise-solutions.ipynb)                | [./ch06](./ch06)                                        |
| 第7章: 指示に応答するようにファインチューニングする            | - [ch07.ipynb](ch07/01_main-chapter-code/ch07.ipynb)<br/>- [gpt_instruction_finetuning.py](ch07/01_main-chapter-code/gpt_instruction_finetuning.py)（まとめ）<br/>- [ollama_evaluate.py](ch07/01_main-chapter-code/ollama_evaluate.py)（まとめ）<br/>- [exercise-solutions.ipynb](ch07/01_main-chapter-code/exercise-solutions.ipynb) | [./ch07](./ch07)                                        |
| 付録A: PyTorch入門                                            | - [code-part1.ipynb](appendix-A/01_main-chapter-code/code-part1.ipynb)<br/>- [code-part2.ipynb](appendix-A/01_main-chapter-code/code-part2.ipynb)<br/>- [DDP-script.py](appendix-A/01_main-chapter-code/DDP-script.py)<br/>- [exercise-solutions.ipynb](appendix-A/01_main-chapter-code/exercise-solutions.ipynb) | [./appendix-A](./appendix-A)                            |
| 付録B: 参考文献とさらなる学習リソース                         | コードなし                                                                                                                                                                                                                             | -                                                       |
| 付録C: 演習問題の解答                                         | コードなし                                                                                                                                                                                                                             | -                                                       |
| 付録D: 学習ループに様々な機能を追加する                       | - [appendix-D.ipynb](appendix-D/01_main-chapter-code/appendix-D.ipynb)                                                                                                                                                                 | [./appendix-D](./appendix-D)                            |
| 付録E: LoRAを使ったパラメータ効率の高いファインチューニング    | - [appendix-E.ipynb](appendix-E/01_main-chapter-code/appendix-E.ipynb)                                                                                                                                                                 | [./appendix-E](./appendix-E)                            |

<br>
&nbsp;

下図の「メンタルモデル」は本書でカバーしている内容をまとめたものです。

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/mental-model.jpg" width="650px">

<br>
&nbsp;

## ハードウェア要件

本書のメイン章で紹介するコードは、専門的なハードウェアを必要とせず、一般的なノートパソコン上で実行できるように設計されています（計算時間も現実的な範囲）。また、もしGPUが使用可能であれば、自動的にGPUを利用します。（追加情報については、[setup](https://github.com/rasbt/LLMs-from-scratch/blob/main/setup/README.md) ドキュメントを参照してください。）

&nbsp;
## ボーナスマテリアル

いくつかのフォルダには、興味がある方のための追加資料が含まれています。

- **セットアップ**
  - [Python関連セットアップのヒント](setup/01_optional-python-setup-preferences)
  - [この書籍で使用しているPythonパッケージやライブラリのインストール](setup/02_installing-python-libraries)
  - [Docker環境セットアップガイド](setup/03_optional-docker-environment)
- **第2章: テキストデータの扱い方**
  - [Byte Pair Encoding (BPE) トークナイザをスクラッチから実装する](ch02/05_bpe-from-scratch/bpe-from-scratch.ipynb)
  - [様々なByte Pair Encoding (BPE) 実装の比較](ch02/02_bonus_bytepair-encoder)
  - [埋め込み層と線形層の違いを理解する](ch02/03_bonus_embedding-vs-matmul)
  - [シンプルな数値例を使ったDataloader](ch02/04_bonus_dataloader-intuition)
- **第3章: アテンションメカニズムをコーディングする**
  - [効率的なマルチヘッドアテンション実装の比較](ch03/02_bonus_efficient-multihead-attention/mha-implementations.ipynb)
  - [PyTorchのバッファーを理解する](ch03/03_understanding-buffers/understanding-buffers.ipynb)
- **第4章: GPTモデルをスクラッチで実装する**
  - [FLOPSの分析](ch04/02_performance-analysis/flops-analysis.ipynb)
- **第5章: ラベルなしデータでの事前学習**
  - [Hugging Face Model Hub と Transformersを使用した代替ウェイト読み込み](ch05/02_alternative_weight_loading/weight-loading-hf-transformers.ipynb)
  - [Project GutenbergデータセットでのGPT事前学習](ch05/03_bonus_pretraining_on_gutenberg)
  - [学習ループに様々な機能を追加する](ch05/04_learning_rate_schedulers)
  - [事前学習のハイパーパラメータを最適化する](ch05/05_bonus_hparam_tuning)
  - [事前学習済みLLMとやり取りできるユーザーインターフェースを構築する](ch05/06_user_interface)
  - [GPTをLlamaに変換する](ch05/07_gpt_to_llama)
  - [Llama 3.2をスクラッチから実装する](ch05/07_gpt_to_llama/standalone-llama32.ipynb)
  - [メモリ効率の良いモデルウェイト読み込み](ch05/08_memory_efficient_weight_loading/memory-efficient-state-dict.ipynb)
  - [TiktokenのBPEトークナイザに新しいトークンを追加する](ch05/09_extending-tokenizers/extend-tiktoken.ipynb)
  - [PyTorchのパフォーマンスを高めてLLMの学習を高速化するヒント](ch05/10_llm-training-speed)
- **第6章: 分類タスクへのファインチューニング**
  - [異なる層のファインチューニングや大きなモデルを使った追加実験](ch06/02_bonus_additional-experiments)
  - [50kのIMDB映画レビュー・データセットを使って様々なモデルをファインチューニング](ch06/03_bonus_imdb-classification)
  - [GPTベースのスパム分類器とやり取りできるユーザーインターフェースを構築する](ch06/04_user_interface)
- **第7章: 指示に応答するようにファインチューニングする**
  - [類似度の高い重複データの検出や受け身表現のレコードを作成するデータセットユーティリティ](ch07/02_dataset-utilities)
  - [OpenAI API と Ollama を使った指示応答の評価](ch07/03_model-evaluation)
  - [指示ファインチューニング用のデータセットを生成する](ch07/05_dataset-generation/llama3-ollama.ipynb)
  - [指示ファインチューニング用データセットの改善](ch07/05_dataset-generation/reflection-gpt4.ipynb)
  - [Llama 3.1 70B と Ollamaを使用してプリファレンスデータセットを生成する](ch07/04_preference-tuning-with-dpo/create-preference-data-ollama.ipynb)
  - [LLMアライメントのためのDirect Preference Optimization (DPO)](ch07/04_preference-tuning-with-dpo/dpo-from-scratch.ipynb)
  - [指示に応答できるようにファインチューニングされたGPTモデルとやり取りするユーザーインターフェースを構築する](ch07/06_user_interface)

<br>
&nbsp;

## 質問、フィードバック、そしてこのリポジトリへの貢献について

Manningの[フォーラム](https://livebook.manning.com/forum?product=raschka&page=1)や[GitHub Discussions](https://github.com/rasbt/LLMs-from-scratch/discussions)で、どんなフィードバックでも歓迎しています。同様に、質問やアイデアの共有も遠慮なく投稿ください。

ただし、このリポジトリは印刷書籍のコードを扱っているため、メインの章コード自体を拡張するようなプルリクエストは（印刷された内容との乖離を避けるために）受け付けていません。読者の皆さんが本と一貫した内容をスムーズに体験できるようにしたいからです。

&nbsp;
## 引用について

もし本書や本コードが研究等で役立った場合には、引用を検討していただけると幸いです。

Chicagoスタイル引用:

> Raschka, Sebastian. *Build A Large Language Model (From Scratch)*. Manning, 2024. ISBN: 978-1633437166.

BibTeXエントリ:

```
@book{build-llms-from-scratch-book,
  author       = {Sebastian Raschka},
  title        = {Build A Large Language Model (From Scratch)},
  publisher    = {Manning},
  year         = {2024},
  isbn         = {978-1633437166},
  url          = {https://www.manning.com/books/build-a-large-language-model-from-scratch},
  github       = {https://github.com/rasbt/LLMs-from-scratch}
}
```
