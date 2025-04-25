# Gherkin to HTML ドキュメント生成ツール

このプロジェクトは、Gherkin形式（.feature）のファイルからHTMLドキュメントを生成するためのツールセットです。Dockerを使用して環境を簡単に構築し、2つの異なるツール（SpecFlow+ LivingDocとPickles）を活用してドキュメント生成が可能です。

## 概要

- **SpecFlow+ LivingDoc**: BDDのシナリオをビジュアル化された「Living Documentation」に変換
- **Pickles**: Gherkinファイルを動的HTMLドキュメントに変換

## 前提条件

- Docker と Docker Compose がインストールされていること
- 変換したい Gherkin (.feature) ファイルがあること

## 使い方

### 1. Gherkinファイルの準備

`features/` ディレクトリに `.feature` ファイルを配置します。サンプルとして `example.feature` が含まれています。

### 2. HTMLドキュメントの生成

#### ローカル環境での生成

##### LivingDocを使用する場合

```bash
docker-compose up livingdoc-generator
```

生成されたHTMLは `html-output/` ディレクトリに保存されます。

##### Picklesを使用する場合

```bash
docker-compose up pickles-generator
```

生成されたHTMLは `pickles-output/` ディレクトリに保存されます。


## プロジェクト構成

```
├── docker/
│   ├── livingdoc/    - LivingDoc用のDockerfile
│   └── pickles/      - Pickles用のDockerfile
├── features/         - Gherkinファイル置き場
│   └── example.feature  - サンプルファイル
├── html-output/      - LivingDocの出力ディレクトリ
├── pickles-output/   - Picklesの出力ディレクトリ
└── docker-compose.yml - Docker Compose設定ファイル
```
