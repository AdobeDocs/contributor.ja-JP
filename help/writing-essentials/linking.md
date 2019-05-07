---
lastModified: '2018-06-28'
title: ドキュメント内でのリンクの使用
seo-title: Adobe Git/Markdown ドキュメント内でのリンクの使用
description: この記事では、コンテンツや画像へのリンクを作成するときのガイドラインを説明します。
seo-description: この記事では、アドビのドキュメント内でコンテンツや画像へのリンクを作成するときのガイドラインを説明します。
translation-type: ht
source-git-commit: 9060d24142e0f03283b42a2a4bbc638abe2952aa

---


# ドキュメント内でのリンクの使用

この記事では、ドキュメントページでのハイパーリンクの使用について説明します。リンクをマークダウンに追加することは簡単にできますが、いくつかのルールがあります。リンクとは、ユーザーを同じページ内のコンテンツや、他の隣接するページ、外部のサイトおよび URL にジャンプさせる機能です。

> [!IMPORTANT]
> ターゲットがセキュアリンクをサポートしている場合は（大部分はそのはずです）、すべてのリンクをセキュアリンクにする必要があります（`https` と `http` の違い）。

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

<!--
## Bob's link test

<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> File Type </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>A comma-separated values file (such as one created in Excel). This is the file that contains the customer attribute data. See [Link TEST](/help/setup/full-workflow.md) </p> <p> <b>Naming requirements:</b> Ensure that file name extensions do not contain white spaces. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>(Required) The <span class="filepath"> .fin </span> file tells the system that you are finished uploading data. The name of the <span class="filepath"> .fin </span> file must match the name of the <span class="filepath"> .csv </span> file. </p> <p>Adobe recommends creating an empty text file with a <span class="filepath"> .fin </span> extension. An empty file saves space and upload time. </p> <p> <p>Note:  Renaming a <span class="filepath"> .fin </span> file is not allowed after it is uploaded. The <span class="filepath"> .fin </span> file must be uploaded separately and cannot be a renamed, previously uploaded file. </p> </p> <p>After you upload the <span class="filepath"> .fin </span> file in the customer attributes FTP, the system retrieves data quickly (within one minute). This differs from other Adobe FTP-based systems, which pick up data less frequently (around once per hour). </p> <p>The <span class="filepath"> .fin </span> file is not required when using the drag-and-drop upload method. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz </span> or <span class="filepath"> .zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz </span> (gzip) or <span class="filepath"> .zip </span> - for compressed files. A <span class="filepath"> .zip </span> file cannot contain more than one file in the archive. </p> <p> <b>Naming requirements:</b> The name of the <span class="filepath"> .zip </span> or <span class="filepath"> .gz </span> should match the name of the <span class="filepath"> .csv </span>. For example, if your <span class="filepath"> .csv </span> file is <span class="filepath"> crm_small.csv </span>, the <span class="filepath"> .zip </span> file should be <span class="filepath"> crm_small.csv.zip </span>. </p> <p>The .fin file must match the .csv. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->
