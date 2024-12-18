---
title: コードレビュー
titleTemplate: :title - Tuist に貢献する
description: Tuistへの貢献を、コードレビューを通じて学ぶ
---

<h1 id="code-reviews">コードレビュー</h1>

プルリクエストのレビューはよくある貢献の形です。 継続的インテグレーション (CI) によってコードが期待通りに動作することが保証されていても、それだけでは十分ではありません。 設計、コードの構造・アーキテクチャ、テストの品質、タイポなど、自動化できない貢献要素が存在します。 以下の項では、コードレビューのプロセスに関するさまざまな観点を取り上げます。

<h2 id="readability">可読性</h2>

そのコードは意図を明確に示していますか？ **コードの意図を理解するのに時間がかかる場合、そのコードを改善する必要があるでしょう。** コードを理解しやすいよう、より小さく抽象的なコードに分割することを提案しましょう。 代替案として、そして最終手段として、レビュイーはコードの背後にある理由を説明するコメントを追加することができます。 プルリクエストの説明などの文脈がなくても、近い将来にそのコードを理解できるかどうか、自分自身に問いかけてみてください。

<h2 id="small-pull-requests">最小単位のプルリクエスト</h2>

巨大なプルリクエストはレビューが難しく、詳細を見逃しやすくなります。 プルリクエストが大きくなりすぎて管理が難しくなった場合は、作成者に分割するよう提案してください。

> [!NOTE] 例外
> 変更が密接に結びついていて分割できない場合など、プルリクエストを分割できないケースがいくつかあります。 そのような場合、作成者は変更内容とその理由について明確に説明する必要があります。 そのような場合、作成者は変更内容とその理由について明確に説明する必要があります。 そのような場合、作成者は変更内容とその理由について明確に説明する必要があります。

<h2 id="consistency">整合性</h2>

変更がプロジェクト全体と整合性を保っていることが重要です。 整合性の欠如はメンテナンスを複雑にするため、避けるべきです。 ユーザーへのメッセージ出力やエラー報告の方法が既に決まっている場合は、それに従うべきです。 もし作成者がプロジェクトの標準に異議を唱えている場合は、議論を深めるために Issue を作成するよう提案してください。

<h2 id="tests">テスト</h2>

テストは、安心してコードを変更できるようにしてくれます。 テストは、安心してコードを変更できるようにしてくれます。 プルリクエストのコードはすべてテストされ、すべてのテストが通っている必要があります。 良いテストとは、一貫して同じ結果を生み出し、理解しやすく、保守しやすいテストのことです。 レビュワーは実装コードのレビューに多くの時間を費やしますが、テストもコードである以上同様に重要です。 良いテストとは、一貫して同じ結果を生み出し、理解しやすく、保守しやすいテストのことです。 レビュワーは実装コードのレビューに多くの時間を費やしますが、テストもコードである以上同様に重要です。

<h2 id="breaking-changes">破壊的な変更</h2>

破壊的な変更はTuistのユーザーにとって悪いユーザー体験です。 どうしても避けられない場合を除き、破壊的な変更を含む貢献は避けてください。 破壊的な変更に頼らなくとも、Tuistのインターフェイスを進化させるために活用できる言語機能はたくさんあります。 破壊的な変更であるかが分かりづらい場合があるかもしれません。 fixturesディレクトリ内のfixtureプロジェクトに対してTuistを実行することでその変更が破壊的変更であるかを確認することができます。 ユーザーの立場に立ち、変更がユーザーにとってどのような影響を与えるかを想像しましょう。 どうしても避けられない場合を除き、破壊的な変更を含む貢献は避けてください。 破壊的な変更に頼らなくとも、Tuistのインターフェイスを進化させるために活用できる言語機能はたくさんあります。 破壊的な変更であるかが分かりづらい場合があるかもしれません。 fixturesディレクトリ内のfixtureプロジェクトに対してTuistを実行することでその変更が破壊的変更であるかを確認することができます。 ユーザーの立場に立ち、変更がユーザーにとってどのような影響を与えるかを想像しましょう。
