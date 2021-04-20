---
lastModified: 2018-06-28T00:00:00Z
title: ドキュメント内でのリンクの使用
seo-title: Adobe Git/Markdown ドキュメント内でのリンクの使用
description: この記事では、コンテンツや画像へのリンクを作成するときのガイドラインを説明します。
seo-description: この記事では、アドビのドキュメント内でコンテンツや画像へのリンクを作成するときのガイドラインを説明します。
exl-id: f9d61aa9-931c-4654-ab21-c6e47936954e
translation-type: ht
source-git-commit: dad1df81797e6078645449501ed0661cf4bcf3ce
workflow-type: ht
source-wordcount: '340'
ht-degree: 100%

---

# ドキュメント内でのリンクの使用

この記事では、ドキュメントページでのハイパーリンクの使用について説明します。リンクをマークダウンに追加することは簡単にできますが、いくつかのルールがあります。リンクとは、ユーザーを同じページ内のコンテンツや、他の隣接するページ、外部のサイトおよび URL にジャンプさせる機能です。

>[!IMPORTANT]
>ターゲットがセキュアリンクをサポートしている場合は（大部分はそのはずです）、すべてのリンクをセキュアリンクにする必要があります（`https` と `http` の違い）。

## URL へのリンク

リンクテキストに含める単語は、リンク先ページのタイトルか、具体的な説明テキストにする必要があります。

**例：**

- `For more information, see the [overview article](https://github.com/AdobeDocs/target.en/help/overview.md).`

- `For more details, see [Adobe Legal Concerns](https://www.adobe.com/legal).`

## ある記事から別の記事へのリンク

ある記事から同じリポジトリ内の別の記事にインラインリンクを作成するには、次のリンク構文を使用します。

- あるディレクトリ内の記事から同じディレクトリ内の別の記事へのリンク：

   `[link text](article-name.md)`

- あるサブディレクトリからルートディレクトリ内の記事へのリンク：

   `[link text](../article-name.md)`

- あるサブサブディレクトリ（孫ディレクトリ）からルートディレクトリ内の記事へのリンク：

   `[link text](../../article-name.md)`

- ルートディレクトリ内の記事からサブディレクトリ内の記事へのリンク：

   `[link text](./directory/article-name.md)`

- あるサブディレクトリ内の記事から別のサブディレクトリ内の記事へのリンク：

   `[link text](../directory/article-name.md)`

- あるサブサブディレクトリ（孫ディレクトリ）内の記事から別のサブディレクトリの記事へのリンク：

   `[link text](../../directory/article-name.md)`

## アンカーへのリンク

アンカーを作成する必要はありません。記事の公開時に、すべての H2 ヘッダーについてアンカーが自動的に生成されます。必要なのは、H2（##）セクションへのリンクを作成することだけです。

- 同じ記事内の見出しにリンクするには：

   `[link](#the-text-of-the-level2-section-separated-by-hyphens)`

   `[Link to anchors](#links-to-anchors)`

- 同じサブディレクトリ内の別の記事内のアンカーにリンクするには：

   `[link text](article-name.md#anchor-name)`

   `[Configure your profile](overview.md#getting-started)`

- 別のサービスサブディレクトリ内のアンカーにリンクするには：

   `[link text](../directory/article-name.md#anchor-name)`

   `[Configure your profile](../overview.md#configure-your-profile)`

## 画像へのリンク

ベストプラクティスとして、画像とファイルは、それらにリンクする Markdown ファイルと同じレベルの `assets` ディレクトリに保存されます。

- 記事から `assets` サブディレクトリ内の画像へのリンク：

   `![alt text](assets/image-name.png)`

- 記事から `assets/no-localize` サブディレクトリ内の画像へのリンク：

   `![alt text](assets/no-localize/image-name.png)`
