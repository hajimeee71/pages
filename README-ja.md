<!--
  <<< Author notes: Header of the course >>>
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses Creative Commons Attribution 4.0 International.
-->

# GitHub Pages

_GitHub Pagesで、GitHubのリポジトリからサイトやブログを作成しましょう。_

<!--
  <<< Author notes: Start of the course >>>
  Include start button, a note about Actions minutes,
  and tell the learner why they should take the course.
  Each step should be wrapped in <details>/<summary>, with an `id` set.
  The start <details> should have `open` as well.
  Do not use quotes on the <details> tag attributes.
-->

<!--step0-->

GitHub Pages を使えば、プロジェクトのブログ、ドキュメント、レジュメ、ポートフォリオ、その他あらゆる静的コンテンツをホストすることができます。GitHub リポジトリは、簡単に自分自身のウェブサイトとなります。このコースでは、GitHub Pages を使って自分のサイトやブログを立ち上げる方法を紹介します。

- **誰のため？**: 初心者、学生、プロジェクト管理者、小規模事業者
- **学べること**: GitHub Pagesサイトの作り方
- **何を作るか**: ブログ付きの簡単なGitHub Pagesサイトを構築します。静的サイトジェネレータである[Jekyll](https://jekyllrb.com)を使用します。
- **前提知識**: ブランチ、コミット、プルリクエストについて学ぶ必要がある場合は、まずは【GitHub入門】(https://github.com/skills/introduction-to-github) で学習してください。
- **期間**: このコースは5つのステップからなり、1時間以内で完了します。

## コース開始までの流れ

1. この手順の上で、**Use this template**を右クリックし、新しいタブでリンクを開きます。
   ![Use this template](https://user-images.githubusercontent.com/1221423/169618716-fb17528d-f332-4fc5-a11a-eaa23562665e.png)
2. 新規タブで、プロンプトに従って、新しいリポジトリを作成します。
   - 所有者には、個人アカウントまたはリポジトリのホストとなる組織を選択します。
   - パブリックリポジトリを作成することをお勧めします-プライベートリポジトリは [use Actions minutes](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions).
   ![Create a new repository](https://user-images.githubusercontent.com/1221423/169618722-406dc508-add4-4074-83f0-c7a7ad87f6f3.png)
3. 新しいリポジトリが作成されたら、20秒ほど待って、ページを更新してください。新しいリポジトリの README にあるステップバイステップの指示に従います。

<!--endstep0-->

<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

<details id=1>
<summary><h2>ステップ1：GitHub Pagesの有効化</h2></summary>

_GitHub PagesとJekyll :tada:へようこそ!_

まず、この[リポジトリ](https://docs.github.com/en/get-started/quickstart/github-glossary#repository)でGitHub Pagesを有効にすることから始めます。リポジトリ上でGitHub Pagesを有効にすると、GitHubはメインブランチにあるコンテンツを取り込んで、そのコンテンツを元にウェブサイトを公開します。

### :キーボード: アクティビティ: GitHub ページの有効化

1. 新しいブラウザのタブを開き、このタブの説明を読みながら、2番目のタブで手順を進めてください。
1. リポジトリ名の下にある、**Settings**をクリックします。
1. "GitHub Pages" セクションで、Sourceドロップダウンを使用し、**main branch**を選択します。
1. 約_1分_待ってから、このページを更新して次のステップに進みます。
   > GitHub Pages をオンにすると、リポジトリのデプロイメントが作成されます。GitHub Actions は、デプロイを待っている間、反応に1分ほどかかることがあります。今後のステップは20秒程度、このステップはゆっくりめです。

</details>

<!--
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
  Historic note: previous version checked for empty pull request, changed to the correct theme `minima`.
-->

<details id=2>
<summary><h2>ステップ2：サイトの設定</h2></summary>

_GitHub Pagesを起動しました。:tada:_

私が作成した`my-pages`というブランチで作業して、このサイトを素晴らしいものにしましょう :sparkle:

Jekyllは、あなたのサイト、あなたのテーマ、およびあなたのサイトのタイトルやGitHubハンドルなどの再利用可能なコンテンツの設定を保存するために `_config.yml` というタイトルのファイルを使用します。あなたは、リポジトリの**コード**タブで `_config.yml` ファイルを確認することができます。

ブログ用のテーマを使う必要があります。今回の活動では、「minima」という名前のテーマを使用します。

### :keyboard: Activity: サイトを設定する

1. `my-pages`ブランチにある `_config.yml` ファイルをブラウズします。
1. 右上にある、ファイルエディタを開きます。
1. `_config.yml` ファイルに、以下のように `theme:` を **minima** に設定し、表示させます。
    ```yml
    theme: minima
    ```
1. (オプション) 他の設定変数、例えば `title:`、`author:`、`description:` を変更して、さらにサイトをカスタマイズすることができます。
1. 変更をコミットします。
1. 20秒ほど待ってから、このページを更新して次のステップに進みます。


</details>

<!--
  <<< Author notes: Step 3 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
  Historic note: previous version checked the homepage content was not empty.
-->

<details id=3>
<summary><h2>ステップ3：トップページのカスタマイズ</h2></summary>

_テーマ設定、お見事です :sparkles:_

ホームページをカスタマイズするには、`index.md` ファイルか `README.md` ファイルに内容を追記します。GitHub Pages は、まず `index.md` ファイルを探します。あなたのリポジトリには `index.md` ファイルがあるので、それを更新してあなたのパーソナライズしたコンテンツを含めることができます。

### :keyboard: Activity: ホームページを作成する

1. `my-pages`ブランチにある `index.md` ファイルをブラウズします。
1. 右上にある、ファイルエディタを開きます。
1. ホームページに掲載したい内容を入力します。このページではMarkdownのフォーマットを使用することができます。
1.（オプション） `title:` を修正することもできますし、今は無視してもかまいません。次のステップでそれについて説明します。
1. 変更を `my-pages` ブランチにコミットします。
1. 20秒ほど待って、次のステップのためにこのページを更新してください。

</details>

<!--
  <<< Author notes: Step 4 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
  Historic note: previous version checked the file path. Previous version checked the front matter formatting.
-->

<details id=4>
<summary><h2>ステップ4：ブログ記事の作成</h2></summary>

_ホームページが素敵になりましたね :cowboy_hat_face:_

あなたのホームページは素晴らしいです！GitHub PagesはJekyllを使用しています。Jekyllでは、特有の名前のファイルとフロントマターを使用することにより、ブログを作成することができます。ファイルの名前は `_posts/YYYY-MM-DD-title.md` である必要があります。また、フロントマターに `title` と `date` を含める必要があります。

**_フロントマター_とは何ですか**Jekyllファイルが使用する構文は、YAMLフロントマターと呼ばれています。それはあなたのファイルの先頭に次のように書かれます。

```yml
---
title: "ブログへようこそ"
date: 2019-01-20
---
```

フロントマターの設定について、詳しくは [Jekyll frontmatter documentation](https://jekyllrb.com/docs/frontmatter/).

### :keyboard: Activity: ブログ記事の作成

1. `my-pages`ブランチをブラウズします。
1. `Add file` ドロップダウンメニューをクリックし、`Create new file` をクリックします。
1.  ファイル名を `_posts/YYYY-MM-DD-title.md` とします。
1. `YYYY-MM-DD`を今日の日付に置き換えて、最初のブログ記事の`title`を変更します（必要なら）。
   > タイトルを編集する場合は、単語と単語の間にハイフンが入っていることを確認してください。
   > ブログの投稿日が正しい日付の規則に従っていない場合、エラーが表示され、サイトが構築されません。詳しくは、以下をご覧ください。"[Page build failed: Invalid post date](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/troubleshooting-jekyll-build-errors-for-github-pages-sites)".
1. ブログ記事のトップに以下の内容を入力します。
   ```yaml
   ---
   title: "YOUR-TITLE"
   date: YYYY-MM-DD
   ---
   ```
1. `YOUR-TITLE`をブログ投稿のタイトルに置き換える。
1. `YYYY-MM-DD` を今日の日付に置き換えてください。
1. ブログ投稿の下書きを入力します。後でいつでも編集できることを忘れないでください。
1. 変更をブランチにコミットします。
1. 20秒ほど待ってから、このページを更新して次のステップに進みます。

</details>

<!--
  <<< Author notes: Step 5 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

<details id=5>
<summary><h2>ステップ 5: プルリクエストのマージ</h2></summary>

_よくやった、友人 :heart:! あなたのブログは、あっという間にみんなが読むようになりますよ。_

プルリクエストを[マージ](https://docs.github.com/en/get-started/quickstart/github-glossary#merge)できるようになりました!

### :keyboard: Activity: Merge your pull request

1. **プルリクエストをマージする**をクリックします。
1. ブランチ `my-pages` を削除します(オプション)。
1. 20秒ほど待ってから、このページを更新して次のステップに進みます。

</details>

<!--
  <<< Author notes: Finish >>>
  Review what we learned, ask for feedback, provide next steps.
-->

<details id=X>
<summary><h2>完了</h2></summary>

_おめでとうございます！あなたはこのコースを完了しました。_

<img src=https://octodex.github.com/images/constructocat2.jpg alt=celebrate width=300 align=right>

あなたのブログが公開され、配信が開始されました!

ここで、リポジトリで達成したすべてのタスクを振り返ってみましょう。


- GitHub Pages を有効にした。
- あなたは、設定ファイルを使用してテーマを選択しました。
- あなたは、Jekyllの適切なディレクトリ形式とファイルの命名規則について学びました。
- あなたはJekyllで最初のブログ投稿を作成しました

### 次はどうする？

- GitHub Pages のサイト作りを続けてください...私たちは、あなたが考え出したものを見るのが大好きです
- このコースの感想をお聞かせください。[ディスカッションボードにて](https://github.com/skills/.github/discussions).
- [Take another GitHub Skills course](https://github.com/skills).
- [Read the GitHub Getting Started docs](https://docs.github.com/en/get-started).
- 貢献できるプロジェクトを探すには、以下をご覧ください。 [GitHub Explore](https://github.com/explore).

</details>

**Deeple翻訳ツール**で翻訳しました。
https://www.deepl.com/translator

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/skills/.github/discussions) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2022 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [CC-BY-4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)
