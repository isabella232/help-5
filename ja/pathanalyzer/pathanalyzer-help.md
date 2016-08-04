﻿# Path アナライザー概要 {#intro}
Path アナライザーでは、顧客とブランドとのインタラクションの Path を分析することができます。最も効果的/非効果的な Path、最適化の適用が可能な Path を特定することに焦点を当てています。
顧客と<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/campaigns/campaigns/create_and_edit_a_campaign_activity" target="_blank">キャンペーン</a>のインタラクションの際に、顧客が特定の<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/channels/channels" target="_blank">チャネル</a> （Eメール、マーケティング、ソーシャルなど）を通過する Path や、<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/campaigns/goals__events/goals" target="_blank">ゴール</a>、<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/engagement_plans/events" target="_blank">イベント</a>、<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/outcomes/outcomes" target="_blank">結果</a>などのビジネスに不可欠なアクティビティをコンバートする道のりを分析することができます。

## 主要なシナリオ {#scenarios}

### 1. マップを調査する {#scenario1}

[主要な視覚化キューを理解すること](#map-key) またキューの背後にあるデータを理解することは、マップを効果的に読み、パターンを見極めるのに重要です。
以下に挙げる機能は Path 分析を始める際に役立ちます。 
特に本アプリケーションを初めて使用する場合や、どこから始めたらよいか分からない場合に役立ちます。

[レポート機能](#reports) は、コンテキスト ペインから利用可能で、レポート カテゴリー毎に Path を簡単にハイライトします。
例えば、 [エンゲージメント バリュー](#value) を生成しない全ての Path を見たい場合、
「バリュー無しの Path」 カテゴリーを選択し、上位10の Path をクリック スルーします。
 [全部で8つのレポート カテゴリー](#reports) があります。

[ダッシュボード ビュー](#dashboard) は、Path 分析を始めたばかりで、 [他のマップ ビュー](#map-views) にまだ慣れていない場合に役立ちます。
ダッシュボード ビューでは、 [マップ KPIs](#map-kpis) 、 [トップ Path エントリー](#top-path-entries) 、
[注目のPath](#featured-path) を確認することができ、 また、[レポート](#reports) 機能や [ファネル](#funnels) 機能にアクセスすることができます。

別のビューとして、[テーブル ビュー](#table-view) があります。
こちらはエクセルの表示画面によく似ていて、全ての Path と それらの主要指標を表示し、ソートやフィルタリングすることができます。

[指標フィルター](#metrics-filter) は、ダッシュボード ビューを除く全てのビューで利用でき、特定の指標に基づく Path に焦点を当てます。
[バリュー](#value) が高く [訪問](#visits) が低い Path、
[訪問毎のバリュー](#value-per-visit) が高い Path、
または [終了バリュー ポテンシャル](#exit-value-potential) が高い Path のマップの表示にこのフィルターを使うことができます。
このように、マップをフィルターにかけ、良い Path、悪い Path、最適化が必要な Path を表示することができます。

### 2. 特定ページへの、または特定ページからの Path を調査する{#scenario2}

特定のページの名前が分かっている場合、
[Path フィルター](#path-filter) を使い、このページへの Path とこのページからの Path を簡単に全て表示することができ、ページの名前をもとに、Path を作成することができます。
移動先のページが念頭にある場合、Path フィルターにそのページを含めることで、ページAからページBへの全ての Path を取得することができます。
[エクスペリエンス マップ](#experience-maps) では、この方法によりゴールに至る Path をフィルターすることができます。

[シナリオ #1](#scenario1) と同様に、[指標フィルター](#metrics-filter) を使い、主要指標の組み合わせにより、フィルターされたマップをより改善することができます。

フィルターを適用後、フィルターされたマップを[読み込み](#map-key) 、各種ビューを調査することも、[レポート機能](#reports) を活用し、[レポート カテゴリー](#reports) 毎のトップ10の Path を迅速にナビゲートすることもできます。
レポートには、適用した [Path フィルター](#path-filter) と [指標フィルター](#metrics-filter) にマッチした Path のみが表示されます。

### 3. マクロレベル Path 分析 （ゴール、イベント、結果）{#scenario3}

ページ レベルのマップが詳細すぎる場合は、
[エクスペリエンス マップ](#experience-maps) が、<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/channels/channels" target="_blank">チャネル</a>, <a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/campaigns/campaigns/create_and_edit_a_campaign_activity" target="_blank">キャンペーン</a>, <a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/campaigns/goals__events/goals" target="_blank">ゴール</a>, <a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/engagement_plans/events" target="_blank">イベント</a>, そして <a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/outcomes/outcomes" target="_blank">結果</a> を中心とした
マクロ レベルの Path 分析を理解するのに役立ちます。

### 4. キャンペーン または チャネル トラフィックを調査する{#scenario4}

特定の<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/channels/channels" target="_blank">チャネル</a> または <a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/campaigns/campaigns/create_and_edit_a_campaign_activity" target="_blank">キャンペーン</a> を通じ、顧客がどのようにブランドとインタラクションを取っているのかを理解したい場合、
[マップ セレクター](#map-selector) を使い、標準の[チャネル マップ](#channel-maps) の一つを選択することができます。または、興味のあるキャンペーンを中心とした新規の[キャンペーン マップ](#campaign-maps) を作成または配置することができます。[シナリオ #3](#scenario3) にあるように、 [エクスペリエンス マップ](#experience-maps) や、[Path フィルター](#path-filter) を使い、特定のチャネルやキャンペーンからの Path のみを表示することができます。

### 5. 特定のセグメントに焦点を当てたマップを調査する {#scenario5}

特定の顧客セグメントからの Path を調査するには、[新規マップを作成](#how-to-create-a-new-map) し、おなじみの<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/personalization/the_rule_set_editor" target="_blank">ルール設定エディター</a> インターフェースを使い、フィルター フィールドにセグメント ルールを指定します。
新規マップが配置された後、マップ セレクターで選択、デフォルトのマップを調査するのと同じ方法で調査することが可能になります。

### 6. ゴールに至る Path を調査する {#scenario6}

設定されたゴールに至る Path を調査する方法の一つは、デフォルトの
[ゴールを含むエクスペリエンス マップ](#experience-maps) を使用し、[Path filter](#path-filter)でゴールを指定することです。

他の方法としては、特定のゴールのための Path にのみ焦点を当てる新規 [ゴール マップ](#goal-maps) を[作成、配置](#how-to-create-a-new-map)することです。
この方法で、特定のアセットや結果への Path を調査することができます。

## マップ {#maps}

マップは、マップ タイプ と マップ フィルター という二つの主要な属性を持つ Path 分析のための特別なマーケティング定義です。 マップ タイプは、マップを動作させるデータをどのように作成するかを示しています。
[こちら](#map-types) でより詳しく述べられています。 マップ フィルターはオプションですが重要な属性で、
<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/personalization/the_rule_set_editor" target="_blank">ルール設定エディター</a> と豊富な条件を使い、セグメント化されたマップを定義するのに役立ちます。

この二つに加え、各マップは独自の識別子、名前、タイプを持ちます。もちろん、description のような他のオプション属性を含めることもできます。

他のマーケティング定義アイテムと同様に、 [マーケティング管理パネルでマップを作成](#how-to-create-a-new-map) します。

マップは [マップ ビュー](#map-views)で視覚化されます。

## マップ タイプ {#map-types}

マップ タイプは xDB からのインタラクション データがどのように Path 分析に変換されるかを規定します。様々なマップ タイプがデフォルトで利用できます。

### ページ マップ {#page-maps}

ページ マップは、あるインタラクション内の一連のページ訪問から作成されます。
いくつかのサブタイプがデフォルトで利用できます。
サブタイプにより、特定のインタラクション属性（チャネル、キャンペーン、ゴール、アセットなど）に焦点を当てたページ マップを簡単に作成することができます。

#### ゴール マップ {#goal-maps}

ゴール マップにより、特定のゴールに至るページ マップを作成することができます。
特定のゴールが達成された後に訪問されたページは無視されます。

マーケティング管理パネルのゴール マップ定義アイテムのリバース チェックボックスを選択することで、ゴール マップをリバース モードで作成することができます。
リバース ゴール マップは、特定のゴールに至る一連のページをひっくり返し、従来の [インターネット ノード](#internet-node) の代わりに選択されたゴールをマップの出発点として使用します。

#### アセット マップ {#asset-maps}

アセット マップにより、特定のアセットのダウンロードに至るページ マップを作成することができます。
特定のアセットがダウンロードされた後に訪問されたページは無視されます。

マーケティング管理パネルのアセット マップ定義アイテムのリバース チェックボックスを選択することで、アセット マップをリバース モードで作成することができます。
リバース アセット マップは、特定のアセットのダウンロードに至る一連のページをひっくり返し、従来の [インターネット ノード](#internet-node) の代わりに選択されたアセットをマップの出発点として使用します。

#### キャンペーン マップ {#campaign-maps}

キャンペーン マップにより、特定のキャンペーンからの全インタラクションのページ マップを作成することができます。

#### チャネル マップ {#channel-maps}

チャネル マップにより、特定のチャネルからの全インタラクションのページ マップを作成することができます。

#### 結果 マップ {#outcome-maps}

結果 マップにより、特定の結果に至るページ マップを作成することができます。

### エクスペリエンス マップ {#experience-maps}

ページ マップと異なり、エクスペリエンス マップはページに加え、 
<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/channels/channels" target="_blank">チャネル</a>, 
<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/campaigns/campaigns/create_and_edit_a_campaign_activity" target="_blank">キャンペーン</a>, 
<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/campaigns/goals__events/goals" target="_blank">ゴール</a>, 
<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/engagement_plans/events" target="_blank">イベント</a>, and 
<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/outcomes/outcomes" target="_blank">結果</a>, 
などの他のインタラクション属性を含めることができます。
マーケティング管理パネルのエクスペリエンス マップ定義アイテムのチェックボックス オプションで、上記のインタラクション属性を選択します。
このようにエクスペリエンス マップを使い、[ページ マップ](#page-maps)より高レベルな Path 分析に焦点を当てることができます。

3つのエクスペリエンス マップがデフォルトで利用できます。

- ゴールを含むエクスペリエンス マップ。チャネル、キャンペーン（存在する場合のみ）、全てのゴール、結果を含む。

- バリュー ゴールのみを含むエクスペリエンス マップ。チャネル、キャンペーン（存在する場合のみ）、ゴール（エンゲージメント バリューが追加されたゴールを除く）、結果を含む

- ページ イベントを含むエクスペリエンス マップ。チャネル、キャンペーン（存在する場合のみ）、エントリー ページと終了ページのみ、全てのページ イベント、結果を含む。

マーケティング管理パネルから既存のマップを基に、簡単に[新規マップを作成](#how-to-create-a-new-map)することができます。

### サイト固有のマップ {#site-specific-maps}
マップ タイプに加え、マップには **グローバル マップ** または **サイト固有のマップ** があります。グローバル マップは全てのサイトに作成されます。一方サイト固有のマップは特定のサイトにのみ作成されます。マップがグローバルか、サイト固有であるかは、マーケティング管理パネルのPath アナライザーのコンテンツ ツリーの中のマップの場所によって決まります。 全てのグローバル マップは */Maps/Default maps/Global maps* フォルダーに配置され、全てのサイト固有のマップは */Maps/Default maps/Site maps* フォルダーに配置されます。

### カスタム マップ {#custom-maps}

カスタム マップが登録されている場合、*/Maps/Custom maps* フォルダーの中に見つけることができます。

### 新規マップを作成する方法{#how-to-create-a-new-map}

新規マップを作成するには:

1.	ラウンチパッドから [マーケティング管理パネル] を開きます。

2.	[Path アナライザー] アイテムに移動します。

3.	[Path アナライザー] 直下の [マップ] アイテムを展開します。

4.	前述の利用可能な [マップ] タイプに基づき、新規マップ用の該当フォルダーを選択します。

5.	新規 [マップ] アイテムを作成します。

6. 必須の属性およびオプションの属性を指定します。

7. [マップ] アイテムを保存します。

8. [レビュー] タブのワークフロー コマンドの [配置] を使い、新規マップを配置します。

マップの履歴データや実データは、配置の約30分後に作成開始されます。

## マップ セレクター {#map-selector}

マップ セレクター コントロールを使って、多種のマップを選択できます。
また、より多くのマップ メタデータを見ることができ、マップを [お気に入り] に追加することができます。[お気に入り] は自動的に [プロファイル] に保存されます。

### グループ マップ データ {#group-map-data}

マップは [ノード](#node) で構成される [ツリー データ構造](#tree) によって動いています。
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

## マップ キー {#map-key}

以下のマップ キーは、放射、水平、垂直 ツリー ビューに適用します。

マップを読む際、マップの円のサイズや色、ノード間の線は、どの Path がより高い [エンゲージメント バリュー](#value) 、より高い [訪問毎のバリュー](#value-per-visit) または最も多く [訪問された](#visits) かの情報を示しています。

円は [ノード](#node) を示します。 選択したマップ タイプにより、ノードはページ、ゴール、またはその他のマーケティング アクティビティを示します。
円は、サイズと色の視覚プロパティーを持ち、ノードについての情報を提供します。

円のサイズは [ノード](#node)とその全子孫の [エンゲージメント バリュー](#value) の合計を示します。
言い換えると、より大きなノードはより大きな [エンゲージメント バリュー](#value)の合計を示します。

円の色は、 [ノード](#node) の [訪問毎のバリュー](#value-per-visit) をその親の訪問毎のバリューと比較して示します。 これはPath をより詳しく調べる際、指標の中に変化を見分けるのに役立ちます。
円が赤になる場合、 [訪問毎のバリュー](#value-per-visit) は、この [ノード](#node) で減少しています。
円が親より緑になる場合、[訪問毎のバリュー](#value-per-visit) は、この [ノード](#node)で増えています。
円の色は、 兄弟ノード間で [訪問毎のバリュー](#value-per-visit) を比較する際に役立ちます。また、最も高い [訪問毎のバリュー](#value-per-visit) Path が、特定の[ノード](#node) から継続する場所を決定するのに役立ちます。 

濃い灰色で太い線の円は、特別な "[その他のノード](#other-nodes)"を示します。

マップ ノードを繋ぐ線は [ノード](#node) A と [ノード](#node) Bの間の Path を示します。 線は濃さと部分的な陰影の視覚プロパティーを持ち、 [Path](#path) についての情報を提供します。

線の濃さは、[ノード](#node) Bの兄弟と比較して、どのくらいの [訪問](#visits) (トラフィック) が [ノード](#node) A から [ノード](#node) B へ移動したかを示しています。 
これにより、高いトラフィック Pathを容易に識別することができます。

線の部分的な陰影は、線の濃さを補完するもので、線の濃さでは違いが分かりにくい Path 訪問をより分かりやすく示すのに使われます。

一般的なガイドラインとして、[エンゲージメント バリュー](#value) (サイズ) が低いPath、  [訪問毎のバリュー](#value-per-visit) (色) が低い Path への訪問量が多いことを示す小さい円または赤い円の太い線を探します。

### その他のノード {#other-nodes}

ツリー ビュー（放射、水平、垂直）の制限により、
極端なファンアウトを持つ大きなマップを視覚化する際、視覚化の一定レベルに達していないあまり重要ではないノードは、特別な"その他の"ノードとして統合されます。 [テーブル ビュー](#table-view) にはこの制限はありません。

"その他のノード"に統合されたノードのリストは、コンテキスト ペインの [Next] タブを選択、またはノード ポップオーバーの [その他] タブを選択することで、確認することができます。

通常、[Path フィルター](#path-filter) または [指標フィルター](#metrics-filter) を適用することで、マップに表示される "その他のノード" の数を減らすことができます。

## マップ ビュー {#map-views}

マップの分析には5つの異なるビューを利用することができます。
ダッシュボードはデフォルトのビューで、Path 分析の入門的な見識を提供します。[以下に](#dashboard) ダッシュボードについての記述があります。

### 放射ビュー {#radial-view}
放射ビューは、より多くのマップ データをスクリーンに表示することに優れていますが、小さいマップやフィルターされたマップには適していません。
[インターネット ノード](#internet-node) が、このビューの中心になります。

### 垂直ビュー {#vertical-view}
垂直ビューは、小さいマップやフィルターされたマップの表示に適しており、通常、[放射ビュー](#radial-view) に比べ可読性に優れています。
[インターネット ノード](#internet-node) は、このビューの一番上に表示されます。

### 水平ビュー {#horizontal-view}
垂直ビューと同様に、水平ビューは小さいマップの表示に適しており、通常、[放射ビュー](#radial-view) に比べ可読性に優れています。
[インターネット ノード](#internet-node) は、一番左端に表示されます。

### テーブル ビュー {#table-view}
テーブル ビューは他のビューとは異なります。マップ データはテーブルとして簡単には表示できない [ツリー構造](#tree) であるため、テーブル ビューは、[完全なPath](#path) のみを表示します。

## ダッシュボード {#dashboard}

ダッシュボードは、Path 分析の入門的な見識を提供する特別なビューです。

### マップ KPI  {#map-kpis}
ダッシュボードでは、6つの重要業績評価指標（KPI）が利用可能です。デフォルトでは： [訪問](#visits)、[バリュー](#value)、 [訪問毎のバリュー](#value-per-visit)が、
オプションとして： [金銭バリュー](#monetary-value)、 [結果](#outcomes)、 [平均金銭バリュー](#average-monetary-value)が利用可能です。

[結果] 指標はデフォルトでは表示されません。[アプリケーション設定](#application-settings) から有効にすることができます。

各マップKPIは、過去の同じマップの同じ日付範囲の同じ指標と比較して、指標の増減を表示するトレンド インジケーターを持っています。
例えば、現在選択されている日付範囲が今日である場合、トレンド インジケーターは、昨日からのデータを基にします。

### トップ Path エントリー {#top-path-entries}

本リストは、現在のマップのトップ10 Pathの開始点を表示します。
Path アナライザーの用語では、これらは第一レベルのトップ10 [ノード](#node) で、
[バリュー](#value) と [訪問](#visits) 指標の複合でソートされます。


### 注目の Path {#featured-path}

注目のPath は、現在選択されているマップから、最も興味深い主要マーケティング指標一式を持つPathを表示します。注目のPath の選定は、 [終了バリュー ポテンシャル](#exit-value-potential) または [バリュー](#value) と [訪問](#visits)の複合のどちらかを考慮に入れた上、どちらか一方の指標カテゴリーのトップ Pathを選択するアルゴリズムを基にしています。
最適化の機会は比較的短い Path に限られるため、アルゴリズムは最も長い Path を優先します。

### お気に入りファネル {#favorite-funnel}

お気に入りファネルは、特定のマップでお気に入りとして記録されたファネルです。お気に入りファネルはファネル直下のコンテキスト ペインでいつでも変更することができます。お気に入りファネルは、ユーザー プロファイルに保存され、お気に入りとして記録された際のマップと関連付けられています。

## レポート {#reports}

Path アナライザー レポートは、多様なカテゴリーのトップ Path を表示します。
レポートは、現在選択されているマップの中で最も興味深い Path の概要を提供するので、これにより良い Path、悪い Pathを迅速に識別することができます。
デフォルトでは、8つのレポート カテゴリーが利用可能です。
各カテゴリーでは、最大10の Path が選定可能です。

### 最高の訪問 {#highest-visited-report}
最高の [訪問](#visits) を持つ Path

### 最高のバリュアブル {#highest-valuable-report}
最高の[エンゲージメント バリュー](#value) を生成する Path

### 最高の訪問とバリュー{#highest-visitsvalue-report}
最高の[エンゲージメント バリュー](#value) と最高の[訪問](#visits) を生成する Path

### 最高の訪問毎のバリュー{#highest-valuepervisit-report}
最高の [訪問毎のバリュー](#value-per-visit) を生成する Path

### バリューのない Path  {#paths-without-value-report}
顧客が [エンゲージメント バリュー](#value) を生成せず終了した Path 

### 最高の終了バリュー ポテンシャル {#highest-evp-report}
最高の [終了バリュー ポテンシャル](#exit-value-potential) を生成する Path

### 最高の結果 {#highest-outcomes-report}
最高の[結果](#outcomes) 数を生成する Path

### 最高の金銭バリュー {#highest-monetaryvalue-report}
結果から生じる最高のトータル [金銭バリュー](#monetary-value) を生成する Path

## ファネル {#funnels}

ファネルは、顧客が経営目標を実現する方向へ進んでいることを表す一連のステップです。
ビジネスは自らのファネルを定義します。Eコマース サイトであれば、おそらく、実装固有事項に応じて、一連のページ、ページ イベントまたはゴールとして示されるチェックアウト ファネルになります。

Path アナライザーのファネルにより、顧客がゴールや結果をコンバートする方向へ進むアクションや Path を分析することができます。そして、例えば、<a href="https://doc.sitecore.net/sitecore_experience_platform/digital_marketing/personalization/personalization" target="_blank">パーソナライゼーション</a>、
<a href="https://doc.sitecore.net/sitecore_experience_platform/analyzing__reporting/experience_optimization__content_testing/ab_and_multivariate_testing" target="_blank">多変量テスト</a>,
または <a href="https://doc.sitecore.net/sitecore_experience_platform/analyzing__reporting/experience_optimization__content_testing" target="_blank">コンテンツ テスト</a> を実行することにより、Path を最適化し、コンバージョン レートを改善することができます。

ファネル機能は、コンテキスト ペインから利用可能で、マーケティング管理パネルで定義されたファネルを選択したり探すことができます。

ファネルを選択した後、Path アナライザー内のファネルからトラックされたステップを、棒グラフの形で見ることができます。棒グラフでは、ファネルの各ステップを完了した顧客の数、何人の顧客が次の段階に進んだか、を知ることができます。 また、[訪問](#visits)、 [バリュー](#value)、 [訪問毎のバリュー](#value-per-visit) などの主要指標を切り替えることができます。
棒グラフの下には、その他全ての指標のリストが表示され、ファネルのKPIを提供します。これらの指標はファネルの最終ステップから取得されます。
このデータは、ライフタイム カスタマー ジャーニー と対比するものとして、インタラクションの範囲を基に算出されます。.

ファネル名のスター アイコンをクリックすることで、どのファネルもお気に入りとして記録することができます。これにより、[ダッシュボード ビュー](#dashboard) でファネルが表示されます。

選択した Path をファネルとして保存するには、コンテキスト ペインのフッター部分にある [ファネルとして保存] をクリックします。

## マップ フィルター {#map-filters}

2種類のフィルターが利用可能で、特定の Path に焦点を当てることができます。

### Path フィルター {#path-filter}

Path フィルターでは、現在のマップの種類により、ページ、ゴール、またはその他のマーケティング属性のいずれかであるノード名に基づきマップをフィルターすることができます。例えば、顧客がどのように興味を持つページにたどり着いたのかを知るために使用することができます。特定のページを Path フィルターの要素として設定し、[適用] をクリックするだけで、マップはそれに応じてフィルターされます。

Path フィルターでは、ページAからページBへのマップ フィルターも作成することができます。
通常、Path フィルターでは3つ以上の要素を要求されることはありませんが、ここではいくつでも要素を指定することができます。
Path フィルターは、現在のマップにおいて利用可能なデータに基づき、オプションのリストを絞り込みます。

### 指標フィルター {#metrics-filter}

指標フィルターは、次の主要指標によるノードのフィルタリングに焦点を当てています： [訪問](#visits)、 [バリュー](#value)、 [訪問毎のバリュー](#value-per-visit)、[終了バリュー ポテンシャル](#exit-value-potential)

主である [Path フィルター](#path-filter) の副次的機能ですので、指標フィルターは, 現在の [Pathフィルター](#path-filter) にいくつマッチするか、また、異なる指標間の相互関係を表示します。
さらに、 [Path フィルター](#path-filter) なしで指標フィルターを使用することもでき、訪問が少ないノードを除き、現在のマップのノイズを減らすことができます。

最後に、指標フィルターにより、異なる指標間の興味深い相互関係を見つけることができます。Path 最適化対象を見つけるには、以下のような例を使用します:

- 高い [訪問](#visits)だが、低い [バリュー](#value)

- 高い [訪問毎のバリュー](#value-per-visit) だが、低い [訪問](#visits)

- 高い [終了バリュー ポテンシャル](#exit-value-potential)

## マップのエクスポート {#export-map}

どのマップのデータも、アクション メニューから以下の二つのコマンドを使用し、カンマ区切りのデータセットとしてエクスポートすることができます:

- CSVとしてダウンロード

-クリップボードにコピーする

どちらのコマンドも同じフォーマットを使用して動作しており、異なるエクスポート ワークフローを有効にするためにあります。

## アプリケーション メッセージ {#application-messages}

Path アナライザーを使用する際、メッセージ バーに様々なメッセージが表示されます。

### "テーブル ビューが Y 合計の中から トップ X Path を表示する" {#table-top}
このメッセージは、 [テーブル ビュー](#table-view) が非常に大きいマップをレンダリングしている際に表示されます。  [テーブル ビュー](#table-view) は、トップ 500  [完全な Path](#path) のみを表示することができます。 このメッセージに対する推奨アクションは次の通りです： [Path フィルター](#path-filter) または [指標フィルター](#metrics-filter) を使用し、表示されている行数を減らす、マップのデータ範囲間隔を減らす、データがより少ないフィルターされたマップを [作成する](#how-to-create-a-new-map) または [選択する](#map-selector) 

### " X 重要度の低いノードが他のノードと共にグループ化されました" {#other-nodes-message}
このメッセージは、極端なのファンアウトを持つ大きなマップを放射、水平、垂直のいずれかのビューで表示した際に表示されます。マップを正しく表示するには、可視化の特定のレベルに適さない重要度の低いノードを特別な 「その他」 ノードと統合します。[テーブル ビュー](#table-view) にはこの制限はないことにご注意ください。このメッセージに対する推奨アクションは次の通りです： [Path フィルター](#path-filter) または [指標フィルター](#metrics-filter) のどちらか一方を使用し、表示されるノードの数を減らす、マップのデータ範囲間隔を減らす、データがより少ないフィルターされたマップを [作成する](#how-to-create-a-new-map) または [選択する](#map-selector) 

### "選択されたマップは作成中です。データの一部のみ確認できます" {#partial-map}
このメッセージは、現在選択されているマップが最近実行されたが、データの作成処理が完了していない場合に表示されます。 新規に実行されたマップのデータは、マップの実行の約30分後に利用可能になります。

## アプリケーション設定 {#application-settings}

Path アナライザー アプリケーション エクスペリエンスのカスタマイズの際に変更可能なアプリケーション設定は以下の通りです：

- 切り替え効果を有効にする/無効にする

- デフォルトでラベルを表示する/非表示にする

- デフォルトで凡例を表示する/非表示にする

- 結果指標を表示する/非表示にする

- 起動時にヘルプを表示する/非表示にする

- 日付のないデータの選択を許可する

上記の設定は、[設定] の下の [アクション メニュー] から利用できます。

## 用語解説 {#glossary}

### マップ {#map}

Path 分析用のデータをどのように作成するかを記述した特別なマーケティング定義。
配置された各マップは、レポーティング データベースに保存された [ツリー](#tree) を持っています。

### ツリー {#tree}

[ノード](#node) の階層から成る各マップ用のレポーティング データベースに保存されたPath 分析のためのデータ構造。
どのツリーも [インターネット ノード](#internet-node) と呼ばれる特別なルート ノードを必ず持っています。

### ノード {#node}

[ツリー](#tree) の主要な要素。
[インターネット ノード](#internet-node) を除く全てのノードは親ノードを持ち、さらに子ノードを持つことができます。
[マップ タイプ](#map-types) に応じて、ノードは ([ページ マップ](#page-maps)の) ページまたはゴールか、または [エクスペリエンス マップ](#experience-maps) のその他のマーケティング属性（チャネル、キャンペーンなど）かのどちらか一方を示すことができます。

各ノードは独自の数値ID、名前、コンテンツ データベースからのアイテムに相当するGUIDを持ちます。

各ノードに保存された各種指標は以下の通りです： 

- **集計指標** は [バリュー](#value)、 [訪問](#visits)、[平均時間](#average-time-spent)、[結果](#outcomes)、 [金銭バリュー](#monetary-value) を含みます。
これらの指標は全ての子孫ノードからのバリューを含みます。

- **終了指標 ** は [終了](#exits) 、[終了バリュー](#exit-value) を含みます。
これらの指標は全ての子孫ノードからのバリューを含まず、現在のノードが [終了ノード](#exit-node) の場合にのみ算出されます。

- **算出指標** は [訪問毎のバリュー](#value-per-visit)、[訪問毎の終了バリュー](#exit-value-per-visit)、 [平均金銭バリュー](#average-monetary-value)、[出口バリュー ポテンシャル](#exit-value-potential) を含みます。

### 終了ノード {#exit-node}

0より大きい [終了](#exits) を持つノード。このノードで終了する [訪問](#visits) 数を示します。

### インターネット ノード {#internet-node}

全ての [Path](#path) の開始ノードとしての役割を持つ特別なルート [ノード](#node) で、特定の [マップ](#map) の全ての Path から全ての主要指標を集計します。

### Path {#path}

一連の [ノード](#node) が Path を生成します。[ツリー](#tree) の性質により、**エントリー Path** と **完全な Path** の2種類のPath を識別することは重要です。

**完全な Path** は、エントリー ノードから [終了ノード](#exit-node) までの全訪問で構成されます。
一方、**エントリー Path**は、終了で終わる必要がありません。
[テーブル ビュー](#map-views) と [レポート機能](#reports) は、完全な Path でのみ動作しますので、この2種類の Path の違いを理解することは重要です。


### 訪問指標 {#visits}

特定のノードの訪問合計。全ての子孫ノードからの訪問指標を含みます。

### バリュー指標 {#value}
特定のノードのエンゲージメント バリュー合計。全ての子孫ノードからのバリュー指標を含みます。

### 訪問毎のバリュー指標 {#value-per-visit}

特定のノードの [訪問](#visits) で割った [エンゲージメント バリュー](#value)。
この指標は **効率** として定義される場合があります。
この指標は [終了バリュー ポテンシャル](#exit-value-potential) を算出するための手段です。

### 終了指標 {#exits}

特定のノードの終了数の合計。
この指標は、特定のノードが 完全な Path または エントリー Pathのどちらから構成されているかを特定します。
0より大きい終了を持つノードは、完全な Path から構成されています。
この指標は、[終了バリュー ポテンシャル](#exit-value-potential) を算出するための手段です。

### 終了バリュー指標 {#exit-value}

特定のノードの終了前のエンゲージメント バリュー。
終了が起こったノードのみこの指標を持ちます。
終了バリュー指標と [バリュー指標](#value)  の違いは、終了バリュー指標が子孫ノードのエンゲージメント バリューを考慮に入れていないことです。

### 訪問毎の終了バリュー指標{#exit-value-per-visit}
特定の [終了ノード](#exit-node) の [訪問](#visits) で割った [エンゲージメント バリュー](#value)。
終了が起こったノードのみこの指標が算出されます。訪問毎の終了バリュー指標と [訪問毎のバリュー](#value-per-visit) 指標の違いは、訪問毎の終了バリュー指標が子孫ノードの訪問毎のエンゲージメント バリューを考慮に入れていないことです。
この指標は、 [終了バリュー ポテンシャル](#exit-value-potential) を算出するための手段です。

### 終了バリュー ポテンシャル指標 {#exit-value-potential}

終了ポテンシャルは、最適化を通じ平均して得られる予測 [エンゲージメント バリュー](#value) を表示します。[終了ノード](#exit-node) にのみ算出されます。
[終了](#exits) に加え、エンゲージメント バリュー 損失 または バリュー漏れもまた考慮される高度な直帰指標として考えることができます。どのくらいの [訪問毎のバリュー](#value-per-visit) が全ての Path に関して計算されているか、また、どのくらいの [訪問毎のバリュー](#value-per-visit) が [終了ノード](#exit-node) に保存されているかが分かっている場合、この指標は二つの差分を取り、終了数で掛けることにより算出することができます。公式は次の通りです：

(訪問毎のバリュー – 訪問毎の終了バリュー) * 終了

### 結果指標 {#outcomes}

特定のノードの実現された結果の総数。全ての子孫ノードからの結果を含みます。
結果についての詳細は<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/outcomes/outcomes" target="_blank">こちら</a> をご確認ください。

### 金銭バリュー指標 {#monetary-value}

特定の [ノード](#node) の得られた金銭バリューの合計。
金銭バリューは実現された結果から取得されます。全ての子孫ノードからの金銭バリューを含みます。
結果についての詳細は<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/outcomes/outcomes" target="_blank">こちら</a> をご確認ください。

### 平均金銭バリュー指標 {#average-monetary-value}

特定の [ノード](#node) の結果毎に得られた平均金銭バリュー。金銭バリューは実現された結果から取得されます。全ての子孫ノードからの平均金銭バリューを含みます。
結果についての詳細は<a href="https://doc.sitecore.net/sitecore_experience_platform/developing/marketing_operations/outcomes/outcomes" target="_blank">こちら</a> をご確認ください。

### 平均時間指標 {#average-time-spent}

特定の [ノード](#node) の顧客が費やした時間の平均（秒）