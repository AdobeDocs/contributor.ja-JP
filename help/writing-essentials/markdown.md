---
title: Markdown を使用してドキュメントを記述する方法
description: この記事では、記事を書くときに使用する Markdown 言語の基礎とリファレンス情報を紹介します。
exl-id: 3e5726e2-139e-4e44-ae5b-8a3ae4782faf
source-git-commit: 9e70d10dc1ba27b593de7febf32a3ba3910bfe21
workflow-type: ht
source-wordcount: '1489'
ht-degree: 100%

---

# Markdown を使用した技術ドキュメントの書き方

アドビの技術ドキュメント記事は、可読性が高く学習しやすい [Markdown](https://daringfireball.net/projects/markdown/) という軽量マークアップ言語で記述されます。

アドビのドキュメントコンテンツは GitHub に保存されるので、Markdown の派生バージョンである [GitHub Flavored Markdown（GFM）](https://help.github.com/categories/writing-on-github/)を使用することができます。GFM は、一般的な書式設定のニーズに応える追加の機能を備えています。さらに、アドビは Markdown に拡張を加えて、メモ、ヒント、埋め込みビデオといったヘルプ関連の機能を使用できるようにしています。

## Markdown の基礎

### 見出し

見出しを作成するには、行の先頭でハッシュマーク（#）を使用します。

```
# This is level 1 (article title)
## This is level 2
### This is level 3
#### This is level 4
##### This is level 5
```

### 基本的なテキスト

Markdown では、段落を示す特別な構文はありません。

テキストを&#x200B;**太字**&#x200B;にするには、2 つのアスタリスクで囲みます。テキストを&#x200B;*斜体*&#x200B;にするには、1 つのアスタリスクで囲みます。

```markdown
   This text is **bold**.
   This text is *italic*.
   This text is both ***bold and italic***.
```

Markdown の書式設定文字を無視するには、その直前で \ を使用します。

```markdown
This is not \*italicized\* type.
```

### 番号付きリストと箇条書きリスト

箇条書きリストを作成するには、行を `1.` または `1)` で始めます。ただし、同じリストで混在させないでください。番号を指定する必要はありません。GitHub によって自動的に番号が振られます。

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

表示：

1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.

箇条書きリストを作成するには、行を \* または - または + で始めます。ただし、同じリストで混在させないでください。（同じドキュメント内で \* や \+ などの箇条書き形式を混在させないでください。）

```markdown
* First item in an unordered list.
* Another item.
* Here we go again.
```

表示：

* First item in an unordered list.
* Another item.
* Here we go again.

リストを入れ子にしたり、リスト項目の間にコンテンツを追加することもできます。

```markdown
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |  
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.
```

表示：

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

### テーブル

テーブルは Markdown のコア仕様には含まれていませんが、アドビのシステムではテーブル機能を一部サポートしています。セル内に複数行のリストを記述することはできません。また、テーブル内に複数行を記述することはお勧めできません。テーブルを作成するには、パイプ文字（|）を使用して行と列を区切ります。列のヘッダーを作成するにはハイフンを使用し、各列をパイプ文字で区切ります。テーブルが正しくレンダリングされるように、テーブルの前には空白行を挿入します。

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

表示：

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

単純なテーブルならば、Markdown でも十分に記述できます。しかし、1 つのセルに複数の段落やリストを含むような複雑なテーブルは記述できません。このようなコンテンツを記述したい場合は、見出しとテキストを使用するなど、別の書式を使用することをお勧めします。

テーブルの作成について詳しくは、以下を参照してください。

* GitHub のヘルプ：[Organizing information with tables（テーブルを使用した情報の整理）](https://docs.github.com/ja/github/writing-on-github/organizing-information-with-tables)
* [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) Web アプリ
* [HTML テーブルから Markdown への変換ツール](https://jmalarcon.github.io/markdowntables/)

### リンク

Markdown のインラインリンクの構文は、ハイパーリンクされるテキストを示す `[link text]` の部分と、それに続くリンク先の URL またはファイル名を示す `(file-name.md)` の部分から構成されます。

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com)
```

表示：

[Adobe](https://www.adobe.com)

リポジトリ内の記事へのリンク（相互参照）を作成するには、相対リンクを使用します。相対リンクのすべてのオペランド、例えば ./（現在のディレクトリ）、../（1 つ上のディレクトリ）、../../（2 つ上のディレクトリ）などを使用できます。

```markdown
See [Overview example article](../../overview.md)
```

リンクの構文の詳細については、このガイドの[リンク](linking.md)の記事を参照してください。

### 画像

```markdown
![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")
```

表示：

![Adobe Logo ](assets/no-localize/adobe_standard_logo.png " Hover text ")

**注意：**&#x200B;ローカライズしない画像の場合は、アセットフォルダーに別の `do-not-localize` フォルダーを作成します。通常は、テキストのない画像やサンプルコンテンツのみを含む画像が配置されます。これで、アセットフォルダーから「ノイズ」が除去され、質問の数が減ります。

### コードブロック

コードブロックの配置については、文中のインラインコードスタイルと、文と文の間に独立して配置される「囲み」コードブロックの両方がサポートされています。詳しくは、[Markdown がネイティブでサポートするコードブロックについての解説を参照してください。](https://daringfireball.net/projects/markdown/syntax#precode)

段落内にインラインコードスタイルを作成するには、バッククォート（`` ` ``）を使用します。複数行から成る特定のコードブロックを作成するには、コードブロックの前後に 3 つのバッククォート（` ``` `）を追加します（Markdown では「囲みコードブロック」、AEM では単に「コードブロック」コンポーネントと呼ばれます）。囲みコードブロックで、コードの構文が正しくハイライトされるようにするには、最初の 3 文字のバッククォートの後にそのコードの言語を追加します。例：` ```javascript`

例：

```markdown
This is `inline code` within a paragraph of text.
```

表示：

This is `inline code` within a paragraph of text.

次に囲みコードブロックの例を示します。

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

## カスタムの Markdown 拡張

アドビのほとんどの記事では、段落、リンク、リスト、見出しといった標準の Markdown を使用します。もっとリッチな書式設定をおこなうには、以下のような Markdown 拡張を使用できます。

* メモブロック
* 埋め込みビデオ
* ローカライズ禁止
* コンポーネントプロパティ（見出しに異なる見出し ID を割り当てるなど）

メモなどの拡張コンポーネントをひとまとめにするには、各行の先頭に Markdown のブロッククォート（>）を使用します。コンポーネント内にサブコンポーネントを入れる必要がある場合は、サブコンポーネントのセクション用に 1 つ深いレベルのブロッククォートを追加します（>  >）。例えば、ローカライズ禁止セクション内にメモを入れるには、メモのセクションを>    > で始めます。

見出しやコードブロックなどの一般的な Markdown 要素には、拡張プロパティが備わっているものもあります。デフォルトプロパティを変更する場合は、コンポーネントの後に中かっこ /{ /} で囲んでパラメーターを追加します。拡張プロパティについては、本文中で説明しています。

### メモブロック

特定のコンテンツに注目を集めるために、これらのタイプのメモブロックを使用できます。

* `[!NOTE]`
* `[!TIP]`
* `[!IMPORTANT]`
* `[!CAUTION]`
* `[!WARNING]`
* `[!ADMINISTRATION]`
* `[!AVAILABILITY]`
* `[!PREREQUISITES]`

メモブロックは文章の流れを妨げることがあるので、多用しすぎないようにします。メモブロックではコードブロック、画像、リスト、リンクも使用できますが、シンプルで簡潔なメモにするよう心がけてください。


```markdown
>[!NOTE]
>
>This is a standard NOTE block.
```

表示：

>[!NOTE]
>
>This is a standard NOTE block.

```markdown
>[!TIP]
>
>This is a standard tip.
```

表示：

>[!TIP]
>
>This is a standard tip.

### ビデオ

埋め込みビデオは Markdown でネイティブにレンダリングされませんが、Markdown 拡張として使用できます。

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

表示：

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

### その他の類似項目

AEM の「その他の類似項目」コンポーネントは、記事の末尾に表示されます。これは関連リンクを示すコンポーネントです。このコンポーネントは記事のレンダリング時にレベル 2 の見出し（##）と同じ書式で表示されますが、ミニ目次には追加されません。

```markdown
>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)
```

表示：

>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/jp/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/jp/support/audience-manager.html)


### UICONTROL と DNL

マークダウンのすべてのヘルプコンテンツは、初めに機械翻訳を使用してローカライズされます。ローカライズされていないヘルプの場合は、機械翻訳のままとなります。ただし、過去にローカライズされたヘルプコンテンツの場合、そのコンテンツが人によって翻訳されている間、機械翻訳されたコンテンツがプレースホルダーとして機能します。

**``**

機械翻訳中、 `` のタグが付けられた項目はローカライゼーションデータベースと照合され、適切な翻訳であるかどうかが確認されます。UI がローカライズされていない場合、このタグを使用すると、特定の言語の UI 参照（イタリア語の Analytics リファレンスなど）が英語のままになります。

**例：**

1. **[!UICONTROL Run Process]**&#x200B;画面に移動します。
1. **[!UICONTROL File > Print > Print All]**&#x200B;を選択して、サーバー上のすべてのファイルを印刷します。
1. [!UICONTROL Processing Rules]ダイアログボックスが開きます。

**ソース：**

```markdown
1. Go to the **[!UICONTROL Run Process]** screen.
1. Choose **[!UICONTROL File > Print > Print All]** to print all the files on your server.
1. The [!UICONTROL Processing Rules] dialog box appears.
```

**注意：** 3 つのタグ付けオプションのうち、高品質を実現するために最も重要かつ必須のオプションです。

**`[!DNL]`**

原則として、英語のまま残す部分を機械翻訳エンジンに通知する際には「翻訳対象外」リストを使用します。最も一般的な項目は「Adobe Analytics」、「Adobe Campaign」、「Adobe Target」などの長いソリューション名です。ただし、その用語が特定の方法や一般的な方法で使用される可能性があるため、英語のまま残すようエンジンに指示する必要がある場合もあります。最もわかりやすい例は、「Analytics」、「Campaign」、「Target」といったソリューションの短い名前です。機械は、それが一般的な用語ではなくソリューション名であることを理解するのを苦手としています。また、このタグは、常に英語で表示するサードパーティの名前や機能、または英語で表示する必要があるフレーズや文といった短い節のテキストにも使用できます。

**例：**

* [!DNL Target] を使用すると、最適なものを見つける A／B テストを作成できます。
* Adobe Analytics は、サイトに関する分析を収集するための強力なソリューションです。[!DNL Analytics] では、レポートを使用して、そのデータのダイジェストを容易に作成することもできます。

**ソース：**

```markdown
* With [!DNL Target], you can create A/B tests to find the optimal 
* Adobe Analytics is a powerful solution to collect analytics on your site. [!DNL Analytics] can also help you with reporting to easily digest that data.
```

## 注意事項とトラブルシューティング

### 代替テキスト

アンダースコアを含む代替テキストは、正しくレンダリングされません。例えば、次のような書き方は避けてください。

```markdown
![Settings_Step_2](/assets/settings_step_2.png)
```

ベストプラクティスとして、ファイル名にはアンダースコア（_）ではなく、ハイフン（-）を使用するようにします。

```markdown
![Settings-Step-2](/assets/settings-step-2.png)
```

### アポストロフィと引用符

テキストを Markdown エディターにコピーする場合、そのテキストに「スマート」（カーリー）アポストロフィまたは引用符が含まれていることがあります。これらの記号はエンコードするか、基本の（ストレートな）アポストロフィまたは引用符に変更する必要があります。そうしないと、ファイルをパブリッシュしたときに Itâ€™s のような文字化けが生じます。

「スマート」バージョンの記号をエンコードするには、以下のようにします。

* 左（開始）引用符：`&#8220;`
* 右（終了）引用符：`&#8221;`
* 右（終了）単一引用符またはアポストロフィ：`&#8217;`
* 左（開始）単一引用符（ほとんど使用されません）：`&#8216;`

### 山かっこ

ファイル内のコードではなく本文テキストで山かっこを使用する場合は（プレースホルダーを表す場合など）、山かっこを手動でエンコードする必要があります。そうしないと、HTML タグであると解釈されます。

例えば、`<script name>` は次のようにエンコードします。`&lt;script name&gt;`

### タイトル内のアンパサンド

タイトル内でアンパサンド（&amp;）を使用することはできません。代わりに、「および」のように書くか、`&amp;` というエンコードを使用します。

## 関連トピック

### Markdown のリソース

* [Markdown 概要](https://daringfireball.net/projects/markdown/syntax)
* [GitHub の Markdown の基礎](https://docs.github.com/ja/github/writing-on-github/getting-started-with-writing-and-formatting-on-github)
