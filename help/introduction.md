---
title: Adobeドキュメントのコントリビューターガイド
seo-title: Contributor guide overview for Adobe Experience Cloud technical documentation
description: このガイドでは、アドビのドキュメントサイトに提案や追加をおこなう方法について説明します。
seo-description: The guide describes how you can contribute to the [!UICONTROL Adobe Experience Cloud] technical documentation.
exl-id: 1294d0c6-897e-49c0-bf27-fd7d122f1fc8
source-git-commit: 8e7d5fb9dc5686df32f7d917ebfb290547d299be
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 98%

---

# Adobeドキュメントのコントリビューターガイド

このガイドでは、Experience League に関するアドビの法人向けヘルプに投稿する方法を説明します。

## コラボレーティブドキュメントとは？

Adobe Experience Cloud やその他のアドビエンタープライズ製品の技術ドキュメントや実施可能性コンテンツは、GitHub、Markdown、Adobe Experience Cloud の各ソリューションを利用するオープンソースの原則に基づいています。

このオープンソースモデルにより、コンテンツの品質、および顧客やドキュメントチーム、製品チーム間のコミュニケーションが向上します。すべてのページで、コンテンツの有用性、問題のログ、および Git プルリクエスト（PR）としてコンテンツの提案事項をコントリビューションできるようになりました。アドビのドキュメントチームは、毎日のコントリビューションと問題を監視し、必要に応じて更新および調整をおこないます。

## 共同作業ドキュメントの操作

従業員、パートナー、顧客、または見込み客に誰であっても、この資料の利用者は、このドキュメントに投稿する方法を、いくつかのシンプルな方法から選択できます。

* ページの有用性を評価する
* 特定のページに対する問題のログ
* アセットやコードのサンプルを使用し、クイック編集を送信して記事全体をオーサリングできます

このガイドでは、操作や、この資料セットにコントリビューションする際に必要なすべての事柄について説明します。

<!--
>[!IMPORTANT]
>All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
-->

## 既存ドキュメントのクイック編集

クイック編集は、ドキュメント内の小さな不備や欠落を修正するのに便利です。記事に以下のような編集ボタンが表示されている場合は、閲覧者がその場で修正できます。文書を編集するときには、修正または提案をアドビに提出するためのプルリクエスト（PR）を送信します。その提案をアドビがレビューして承認し、公開します。

1. 同意できる場合は[コントリビューター使用許諾契約（CLA）](http://opensource.adobe.com/cla.html)に署名します。

   アドビの CLA は 1 回提出すれば済みます。
1. 右列の **[!UICONTROL Edit this page]** をクリックして、GitHub の Markdown ソースファイルに移動します。

   ![このページを編集アイコン](/help/assets/git_edit.png)

1. 鉛筆アイコンをクリックして記事を編集します。

   >[!NOTE]
   >
   >鉛筆アイコンがグレー表示になっている場合は、GitHub アカウントにログインするか、新しいアカウントを作成する必要があります。

   ![鉛筆アイコンの場所](assets/edit-icon.png)

1. Web エディターで変更を加えます。

   「**[!UICONTROL Preview changes]**」タブをクリックすると、変更部分の書式を確認できます。
1. 変更を加えたら、ページの下部までスクロールします。

   PR のタイトルと説明を入力し、次の図に示す **[!UICONTROL Propose file change]** をクリックします。

   ![変更の提案](assets/submit-pull-request.png)

   >[!NOTE]
   >
   >コントリビューター使用許諾契約（CLA）への署名に関する検証エラーメッセージが表示されたら、**[!UICONTROL Details]** をクリックしてライセンス契約書を開きます。同意できる場合は、契約に署名します。次に、プルリクエストを閉じてから開いて続行します。

必要な操作は以上です。いただいたプルリクエストは、ドキュメントチームメンバーがレビューして結合します。ご協力ありがとうございます。

## 問題をログに記録

コンテンツの一部に関する問題を容易に指摘するもう一つの方法は、**[!UICONTROL Log an Issue]** を使用することです。

1. コンテンツの一部で問題を見つけたら、右列にある「**[!UICONTROL Log an Issue]**」アイコンをクリックします。

   ![](assets/git_log_issue.png)

   >[!NOTE]
   >
   >問題をログに記録するには、GitHub アカウントにログインするか、アカウントを作成する必要があります。

   このリンクをクリックすると、GitHub Issue インターフェイスを使用して、Experience League でクイックチケットを登録できます。

   問題を含むページの URL が説明フィールドに自動的に挿入されます。

1. タイトルを入力し、イシューの簡単な説明を書いてから、「*新しいイシューを送信*」をクリックします。

   ![](assets/git_issue_example.png)

イシューを送信すると、このページのコンテンツチームに通知が送られます。このチームはイシューを解決できます。担当チームがコンテンツを更新すると、GitHub Issues インターフェイス上で登録者に通知されます。問題に進展があるか、問題がクローズされると、電子メールで通知されます。

## GitHub の権限について

GitHub の編集 UI は、利用者のリポジトリ権限に応じて変化します。前掲の画像は、ターゲットリポジトリへの書き込み権限を持たないコントリビューターに表示されるものです。GitHub は自動的に利用者のアカウント内にターゲットリポジトリのフォークを作成します。利用者がターゲットリポジトリへの書き込み権限を持っている場合は、GitHub はターゲットリポジトリ内に新しいブランチを作成します。

アドビはすべての変更でプルリクエストを使用します。書き込み権限を持つコントリビューターによる変更でも同様です。ほとんどのリポジトリには保護された`main`ブランチがあり、アップデートはプルリクエストとして送信される必要があります。

ブラウザー内編集の機能は、小さな変更や頻繁でない変更に適しています。大きな変更を加える場合や、高度な Git 機能を使用する場合は、[リポジトリをフォークしてローカルで作業する](setup/full-workflow.md)ことをお勧めします。

## フィードバックの提供

アドビのソリューションセットのように大規模なものになると、ドキュメントは常に作業中になります。エラーを見つけた場合はログに記録し、提案がある場合はアドビまでお知らせください。どのような情報を探しているか、ご意見をお聞かせください。必要な情報が見つからない場合は、その旨をお知らせください。タスクをうまく完了できない場合は、どこがわからないかをご指摘ください。

共同作業ドキュメントの担当チームと Experience League のすべてのライターおよびコンテンツ製作者を代表して、皆様のご協力に感謝を申し上げます。
