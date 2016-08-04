﻿# ページ アナライザー概要 {#intro}
ラウンチパッドから利用できるPath アナライザーは高度なPath分析に焦点を当てていますが、一方、ページ アナライザーは、特定のページへのPath、または特定のページからのPathにのみ焦点を当てています。
ページ アナライザーの主な目的は、顧客がある目的地（ページ）へどのようにたどり着くのか、また、顧客はその後何をするのかを理解することです。
データ視覚化キューにより、最も多いトラフィック（訪問）を持つ Path や、最も高い訪問毎のエンゲージメント バリューを持つ Path を理解することができ、良い Path、悪い Pathを特定することができます。特定の Path を掘り下げ、Path の詳細を調査することも可能です。

## ビジュアル（視覚化）を読み取る方法 {#map-key}
ビジュアル（視覚化）では、現在選択されているページが中心に置かれます（ページ アイコンを持つ大きい円として表示されます）。
このページに入る Path、このページから出る Path、全ての Path が表示されます。

ランディング エリアには、いくつの Path が現在選択されているページから開始したかが表示されます。

終了エリアには、現在選択されているページで終了した数と [終了バリュー ポテンシャル](#exit-value-potential) の累計が表示されます。

現在選択されているページ *へ* 流れる水平の線は、インカミング Path です。
線の上部に置かれている円はそのPathの [ノード](#node) を示します。ノードは通常ページへ変換します。

現在選択されているページ *から* 右へ流れる水平の線は、アウトゴーイング Path です。

線の上部に置かれている円はそのPathの [ノード](#node) を示します。ノードは通常ページへ変換します。
ビジュアル（視覚化）を単純化するため、最初のページのみがアウトゴーイング Path に表示されます。

線の太さは、特定の Path から現在選択されているページへの [訪問](#visits) の総数を定義しています。
Path が太ければ太いほど、選択されているページにより多くの訪問があることになります。

線の色は、この特定の Path から現在選択されているページへの [訪問毎のバリュー](#value-per-visit) を定義しています。
Path の色が緑であればあるほど、現在選択されているページに入る他の Path と比較して、 [訪問毎のバリュー](#value-per-visit) が高いことになります。
訪問毎のバリューが最小の Path は赤で表示されます。

円のサイズは、現在選択されているページに繋がる Path のエンゲージメント バリューの総数を定義しています。
円が大きければ大きいほど、 [エンゲージメント バリュー](#value) は高くなります。

コンテキスト ペイン エリアでは、Path の総数だけでなく、訪問、バリュー、訪問毎のバリュー指標の総計が表示されます。
特定の Path の上にマウス ポインターを置くと、総計エリアにその Path からの指標が表示されます。

## マップ セレクター {#map-selector}

マップ セレクター コントロールを使って、多種のマップを選択できます。
また、より多くのマップ メタデータを見ることができ、マップを [お気に入り] に追加することができます。[お気に入り] は自動的に [プロファイル] に保存されます。

### グループ マップ データ {#group-map-data}

マップは [ノード](#node) で構成されるツリー データ構造によって動いています。
各 [ノード](#node) はコンテンツ（Master）データベースに該当するアイテムを持つので、
マップ セレクターのグループ マップ データ チェックボックスを選択すると、ノードはノードが作成されたSitecore データ テンプレートによりグループ化されます。

例えば、以下の2つのPathを：

- Home -&gt; TVs -&gt; 50" flat screen TV

- Home -&gt; Tablets -&gt; 12" tablet

一つのPathにグループ化することができます：


- Landing Page -&gt; Product Category Page -&gt; Product Detail page

グループ化されたマップ データは、個別のページ レベルよりページ カテゴリー レベルでの Path 分析を行う際に便利です。

## 日付範囲セレクター {#date-selector}

日付範囲セレクターを使用し、カレンダーから個別の開始日、終了日を選択するか、既定の日付範囲から選択することで日付の範囲を選択することができます。

### 日付のないデータ {#date-selector-missing-dates}

ある特定の日付の前後に利用可能なデータがあったとしても、その日付に対する利用可能なデータを持たないマップがある場合があるかもしれません。
これはその日付に記録されたインタラクションがない、またはデータ処理の際にエラーが起き、エラーを含む日付がスキップされたことが原因である可能性があります。
日付範囲セレクターは、利用可能なデータがない日付を表示します。
利用可能なデータがない日付がカレンダーに多く表示された場合は、システム管理者にご連絡ください。

### 利用できない日付 {#date-selector-unavailable-dates}

選択した日付範囲により、いくつかの日付が選択不可と表示される場合があります。
例えば、終了日を選択する際、開始日より前の日付は利用不可と表示されます。
全ての未来日付も利用不可と表示されます。

## 指標フィルター {#metrics-filter}

指標フィルターは、次の主要指標によるノードのフィルタリングに焦点を当てています： 訪問、バリュー、訪問毎のバリュー、終了バリュー ポテンシャル
指標フィルターにより、ノイズを減らしたり、異なる指標間の興味深い相互関係を見つけることができます。また、Path 最適化対象を見つけるには、以下のような例を使用します:

- 高い [訪問](#visits)だが、低い [バリュー](#value).

- 高い [訪問毎のバリュー](#value-per-visit)だが、低い [訪問](#visits).

- 高い [終了バリュー ポテンシャル](#exit-value-potential).

## アプリケーション メッセージ {#application-messages}
ページ アナライザーを使用する際、メッセージ バーに様々なメッセージが表示されます。

### "一部の Path が非表示になっています。他の Path を確認するにはフィルターを使用してください。" {#page-analyzer-hidden-paths}
ページ アナライザーが同時に表示する Path の数は10です。
指標フィルターで、指標の基準に基づき Path の数を減らします。

### " X 件中の 500 の Path に基づきます。" {#page-analyzer-maximum-paths}
ホーム ページなど、一部のページは、ページ全体で独自の Path を大量に持つ場合があります。
効率を良くするために、ページ アナライザーは上位500の Path のみを処理します。
これに対処するには、よりセグメント化されたマップを選択する、または日付の間隔を小さくします。

### "選択されたマップは作成中です。データの一部のみ確認できます。" {#partial-map}
このメッセージは、現在選択されているマップが最近実行されたが、データの作成処理が完了していない場合に表示されます。 新規に実行されたマップのデータは、マップの実行の約30分後に利用可能になります。

## 用語解説 {#glossary}

### マップ {#map}

Path 分析用のデータをどのように作成するかを記述した特別なマーケティング定義。
ページ アナライザーはマップ データを使い、全ての Path をフィルターし、現在選択されているページを通過している Path のみを表示します。
このフィルターされたデータセットは視覚化に使われます。
[マップ セレクター](#map-selector) を使い他のマップへ切り替えることができます。

### Path {#path}

一連の [ノード](#node) が Path を生成します。 ページ アナライザーに表示される全ての Path は現在選択されているページを通過します。

### ノード {#node}

[Path](#path) の要素。 ほとんどのマップにとって、ノードは原則的に他のページへ変換するものです。
一連の指標が各ノードに保存されています：[バリュー](#value)、 [訪問](#visits)、
[訪問毎のバリュー](#value-per-visit)、[終了](#exits)、 [終了バリュー](#exit-value)、 [訪問毎の終了バリュー](#exit-value-per-visit)、 [平均時間](#average-time-spent)

### 終了ノード {#exit-node}

0より大きい[終了](#exits) を持つノード。このノードで終了する[訪問](#visits) 数を示します。

### 訪問指標 {#visits}

特定のノードの訪問合計。全ての子孫ノードからの訪問指標を含みます。

### バリュー指標 {#value}
特定のノードのエンゲージメント バリュー合計。全ての子孫ノードからのバリュー指標を含みます。

### 訪問毎のバリュー指標 {#value-per-visit}

特定のノードの[訪問](#visits) で割った [エンゲージメント バリュー](#value)。
この指標は **効率** として定義される場合があります。
この指標は [終了バリュー ポテンシャル](#exit-value-potential) を算出するための手段です。

### 終了指標 {#exits}

特定のノードの終了数の合計。
この指標は、特定のノードが 完全な Path または エントリー Pathのどちらから構成されているかを特定します。
0より大きい終了を持つノードは、完全な Path から構成されています。
この指標は、[終了バリュー ポテンシャル](#exit-value-potential)を算出するための手段です。

### 終了バリュー指標 {#exit-value}

特定のノードの終了前のエンゲージメント バリュー。
終了が起こったノードのみこの指標を持ちます。
終了バリュー指標と [バリュー指標](#value)  の違いは、終了バリュー指標が子孫ノードのエンゲージメント バリューを考慮に入れていないことです。

### 訪問毎の終了バリュー指標 {#exit-value-per-visit}
特定の [終了ノード](#exit-node) の [訪問](#visits) で割った [エンゲージメント バリュー](#value)。
終了が起こったノードのみこの指標が算出されます。訪問毎の終了バリュー指標と[訪問毎のバリュー](#value-per-visit) 指標の違いは、訪問毎の終了バリュー指標が子孫ノードの訪問毎のエンゲージメント バリューを考慮に入れていないことです。
この指標は、 [終了バリュー ポテンシャル](#exit-value-potential) を算出するための手段です。

### 終了バリュー ポテンシャル指標 {#exit-value-potential}

終了ポテンシャルは、最適化を通じ平均して得られる予測 [エンゲージメント バリュー](#value) を表示します。[終了ノード](#exit-node) にのみ算出されます。
[終了](#exits) に加え、エンゲージメント バリュー 損失 または バリュー漏れもまた考慮される高度な直帰指標として考えることができます。どのくらいの [訪問毎のバリュー](#value-per-visit) が全ての Path に関して計算されているか、また、どのくらいの [訪問毎のバリュー](#value-per-visit) が [終了ノード](#exit-node) に保存されているかが分かっている場合、この指標は二つの差分を取り、終了数で掛けることにより算出することができます。公式は次の通りです：

(訪問毎のバリュー – 訪問毎の終了バリュー) * 終了