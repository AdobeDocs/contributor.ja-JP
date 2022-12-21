---
title: アドビドキュメントのコントリビューターガイド
seo-title: Contributor guide overview for Adobe Experience Cloud technical documentation
description: このガイドでは、アドビのドキュメントサイトに提案や追加をおこなう方法について説明します。
seo-description: The guide describes how you can contribute to the [!UICONTROL Adobe Experience Cloud] technical documentation.
exl-id: 1294d0c6-897e-49c0-bf27-fd7d122f1fc8
source-git-commit: 90122796acee9214ba96360eb7b5ff5c321a4bd6
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 67%

---

# アドビドキュメントのコントリビューターガイド

このガイドでは、Experience Leagueに関する Enterprise ヘルプにAdobeを投稿する方法を説明します。

## コラボレーションドキュメントとは

Adobe Experience Cloudやその他のAdobeエンタープライズ製品の技術ドキュメントやイネーブルメントコンテンツは、GitHub、Markdown、Adobe Experience Cloudの各ソリューションを利用するオープンソースの原則に基づいています。

このオープンソースモデルにより、顧客、ドキュメントチーム、製品チーム間のコンテンツ品質と通信が向上します。 すべてのページで、コンテンツの有用性、問題のログ、および Git プルリクエスト（PR）としてコンテンツの提案事項をコントリビューションできるようになりました。アドビのドキュメントチームは、毎日のコントリビューションと問題を監視し、必要に応じて更新および調整をおこないます。

## コラボレーションドキュメントの操作

従業員、パートナー、顧客、または見込み客を含め、この資料の利用者は、このドキュメントにコントリビューションする方法を、いくつかのシンプルな方法から選択できます。

* ページの有用性を評価
* 特定のページに関する問題のログ
* アセットとコードサンプルを含むクイック編集を送信して、記事全体をオーサリングします

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
1. クリック **[!UICONTROL Edit this page]** 右の列で、GitHub の markdown ソースファイルに移動します。

   ![このページを編集アイコン](/help/assets/git_edit.png)

1. 鉛筆アイコンをクリックして記事を編集します。

   >[!NOTE]
   >
   >鉛筆アイコンがグレー表示になっている場合は、GitHub アカウントにログインするか、新しいアカウントを作成する必要があります。

   ![鉛筆アイコンの場所](assets/edit-icon.png)

1. Web エディターで変更をおこないます。

   「**[!UICONTROL Preview changes]**」タブをクリックすると、変更部分の書式を確認できます。
1. 変更を加えたら、ページの下部までスクロールします。

   PR のタイトルと説明を入力し、「 **[!UICONTROL Propose file change]** 次の図に示すように：

   ![変更の提案](assets/submit-pull-request.png)

   >[!NOTE]
   >
   >コントリビューター使用許諾契約 (CLA) への署名に関する検証エラーメッセージが表示された場合は、 **[!UICONTROL Details]** をクリックして、使用許諾契約を開きます。 同意できる場合は、契約に署名します。次に、プルリクエストを閉じてから開いて続行します。

必要な操作は以上です。提出されたプルリクエストをドキュメントチームメンバーがレビューしてマージします。ご協力ありがとうございます。

## 問題のログ

コンテンツの一部に関する問題を知らせるもう 1 つの簡単な方法は、 **[!UICONTROL Log an Issue]**.

1. コンテンツの一部に問題がある場合は、右列にある「**[!UICONTROL Log an Issue]**」アイコンをクリックします。

   ![](assets/git_log_issue.png)

   >[!NOTE]
   >
   >問題をログに記録するには、GitHub アカウントにログインするか、アカウントを作成する必要があります。

   このリンクをクリックすると、Github Issue インターフェイスを使用して、Experience Leagueのクイックチケットをログに記録できます。

   問題を含むページの URL が説明フィールドに自動的に入力されます。

1. タイトルを入力し、問題の簡単な説明を書いてから、「*Submit new issue*」をクリックします。

   ![](assets/git_issue_example.png)

問題を送信すると、このページのコンテンツチームに通知され、ユーザーが問題に対処できます。 担当チームがコンテンツを更新すると、GitHub Issues インターフェイス上で登録者に通知されます。問題に進展があるか、問題がクローズされると、電子メールで通知されます。

## GitHub の権限について

GitHub の編集 UI は、利用者のリポジトリ権限に応じて変化します。前掲の画像は、ターゲットリポジトリへの書き込み権限を持たないコントリビューターに表示されるものです。GitHub は自動的に利用者のアカウント内にターゲットリポジトリのフォークを作成します。利用者がターゲットリポジトリへの書き込み権限を持っている場合は、GitHub はターゲットリポジトリ内に新しいブランチを作成します。

アドビはすべての変更でプルリクエストを使用します。書き込み権限を持つコントリビューターによる変更でも同様です。ほとんどのリポジトリには保護された`main`ブランチがあり、アップデートはプルリクエストとして送信される必要があります。

ブラウザー内編集の機能は、小さな変更や頻繁でない変更に適しています。大きな変更を加える場合や、高度な Git 機能を使用する場合は、[リポジトリをフォークしてローカルで作業する](setup/full-workflow.md)ことをお勧めします。

## フィードバックの提供

アドビのソリューションセットのように大規模なものになると、ドキュメントは常に作業中になります。エラーを見つけた場合はログに記録し、提案がある場合はアドビまでお知らせください。どのような情報を探しているか、ご意見をお聞かせください。必要な情報が見つからない場合は、その旨をお知らせください。タスクをうまく完了できない場合は、どこがわからないかをご指摘ください。

コラボレーティブドキュメントの担当チームとExperience Leagueのすべてのライターおよびコンテンツプロデューサーを代表して、皆様のご協力に感謝を申し上げます。
