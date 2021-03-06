# 更新履歴

 - master/HEAD
 - 0.8.2015111101
   * タブ選択時のメニューが自動的に閉じられた場合でも「選択を反転」が正しく動作するようにした
   * [`ru`ロケール更新（by Infocatcher, thanks!）](https://github.com/piroor/multipletab/pull/102)
 - 0.8.2015111001
   * Firefox 40以降に対応
   * タブのコンテキストメニューに「似たタブを全て選択」、選択時のメニューに「選択を反転」を追加した
   * 選択されたタブをブックマークフォルダとして保存する機能およびブックマークフォルダのプロパティ編集が動作しなくなっていたのを修正
   * タブのプロセス分離の状態が変更された後もコンテンツ領域内からのメッセージを正しく受け取るように修正
 - 0.8.2015030601
   * タブのクローズボックス上でのクリック操作を、他の一般的なボタンと同様に、ドラッグしてそのままクローズボックス外でマウスのボタンを放す事でキャンセルできるようにした（[まとめて閉じるタブの選択操作を、2番目のタブのクローズボックス上にポインタが載った時点で初めて開始するようにした](https://github.com/piroor/multipletab/issues/22#issuecomment-77101283)）
 - 0.8.2015022701
   * Firefox 36以降で動作するように修正
   * 複製したタブを、複製元タブの隣に開くようにした
   * Ctrl-ドラッグ＆ドロップで同じウィンドウの中にタブを複製できなくなっていたのを修正
   * Ctrl-ドラッグ＆ドロップで別のウィンドウからタブを引くせいできなくなっていたのを修正
   * 復元可能な数のタブよりも少ない数のタブを一度に閉じようとしている時は警告を表示しないようにした
   * `extensions.multipletab.tabdrag.delay`の設定が機能しなくなっていたのを修正([By Infocatcher](https://github.com/piroor/multipletab/pull/84). Thanks!)
 - 0.8.2014102201
   * Firefox 30およびそれ以前のバージョンのサポートを終了
   * マルチプロセスモード（E10S）に対応
   * 「タブのクローズボックスをドラッグして選択した場合、タブをまとめて閉じる」機能の有効・無効を切り替えるオプションを追加
   * 選択したタブのロック状態を変更できない問題を修正
   * Nightly 33.0a1において `dom.compartment_per_addon`=`true` に設定した場合でも動作するように暫定的に対処
 - 0.7.2014050101
   * Linux上のAustralisにおいて、まとめて閉じられようとしているタブの表示が見にくかったのを修正
 - 0.7.2014043001
   * Tab Mix Plusとの併用時に初期化に失敗する問題を修正（後退バグ）
 - 0.7.2014042701
   * Firefox 31.0a1に対応
   * Firefox 23より古いバージョンのサポートを終了
   * 待機状態のタブのURI等をコピーする時、必要のない限りはタブの内容を読み込まないようにした
 - 0.7.2013100801
   * Firefox 24以降の「右のタブを閉じる」機能に対応（Firefox自身が機能を提供している場合、マルチプルタブハンドラ自体の機能は無効化されます）
   * Firefox 25に対応
 - 0.7.2013052901
   * 「グループに移動」のポップアップに、名前が付いていないグループも表示するようにした
   * 選択したタブをコピーする機能において、リッチテキスト形式でのコピーに対応した（「%RT%」というキーワードをフォーマット中で指定すると、結果がリッチテキストHTMLとしてコピーされます）（by Yue Hu (ximellon). Thanks!）
   * 「タブのURIをコピー」機能で利用できるプレースホルダのヘルプ文字列をより読みやすい形に整形（by Infocatcher. Thanks!）
   * [セッション保存APIの仕様変更](http://dutherenverseauborddelatable.wordpress.com/2013/05/23/add-on-breakage-continued-list-of-add-ons-that-will-probably-be-affected/)に追従
 - 0.7.2013040601
   * Firefox 19以降で複数のタブをウィンドウ外にドラッグして新しいウィンドウに移動する時に、他のタブが追従しない問題を修正
   * "ru"ロケール更新 (by Infocatcher)
   * "zh-TW"ロケール更新 (by HJL)
   * jarファイルを含めない形のパッケージングに変更
 - 0.7.2012122901
   * Nightly 20.0a1に対応
   * 選択したタブをコピーする機能において、水平タブのための新しい特殊文字指定「%TAB%」を利用できるようにした
   * [Suspend Tab](http://piro.sakura.ne.jp/xul/_suspendtab.html)および[UnloadTab](https://addons.mozilla.org/firefox/addon/unloadtab/)との併用時に、選択したタブに対してまとめて「タブをサスペンド」「タブを復帰」を実行できるようにした
   * 選択したタブを保存する機能が動かなくなっていたのを修正（リグレッション）
   * 選択された複数のタブのうち1番目以外のタブをドラッグしてタブの移動を開始した場合に、タブの移動に失敗していたのを修正
   * 最近のバージョンのFirefoxにおいて、複数のタブを選択してウィンドウ外にドロップした時に、ドラッグ操作が開始されたタブ以外のタブが新しいウィンドウに移動しなくなっていたのを修正
 - 0.7.2012111301
   * 選択したタブをリロードする機能が正しく動いていなかったのを修正
   * 選択したタブを保存する機能が最近のNightlyで動かなくなっていたのを修正
   * 選択したタブを保存する機能がWindows上で時々失敗する事があったのを修正
 - 0.7.2012111001
   * Nightly 19.0a1へ対応
   * Firefox 10よりも古いバージョンへの対応を終了
   * 複数タブのドラッグ＆ドロップ時にアニメーション効果を正しく適用するようにした（Firefox 17以降）
   * 選択されたタブを新しいウィンドウに切り離すなどの、複数のタブに対する一括操作によって、まだ復元されていないタブの内容が失われる問題を修正（安全に復元するようになりました）
   * ユーザがまだタブグループ機能を使った事が無い場合には、タブのコンテキストメニューで「グループに移動」を隠すようにした
   * Shift-クリックで期待と異なるタブが選択される場合があったのを修正
 - 0.7.2012020901
   * Nightly 13.0a1へ対応
   * Firefox 3.6への対応を終了
   * 選択されたタブに対するコンテキストメニューにおいて、いくつかの項目の表示・非表示に関してユーザ設定が反映されていなかったのを修正
   * 最近のNightlyにおいて選択されたタブからブックマークを作成できなくなっていたのを修正
 - 0.6.2011120101
   * クローズボックスの上でのドラッグの開始について、開始までの待ち時間を設定できるようにした（待ち時間は隠し設定「extensions.multipletab.tabdrag.close.delay」にて変更可能。初期値は「0」。)
   * Tab Mix Plusと併用した時にCtrl/Shift-クリックの設定の競合を自動的に解消した場合、マルチプルタブハンドラまたはTab Mix Plusを無効化あるいは削除した時に以前の設定を自動的に復元するようにした
   * ファイル選択時の挙動と同様に、複数のタブが選択された状態でそのうちの1つをクリックした時も選択を解除するようにした
   * クローズボックスの外周1ピクセル分の領域で意図せずドラッグ操作に反応してしまっていたのを修正
 - 0.6.2011092901
   * 註：このバージョンおよびこれ以前のバージョンは、[bug 455694](https://bugzilla.mozilla.org/show_bug.cgi?id=455694)および[bug 674925](https://bugzilla.mozilla.org/show_bug.cgi?id=674925)の影響によりFirefox 8以降には非対応です
   * ドラッグ操作でタブを選択または閉じようとしている間にESCキーを押した時に、操作をキャンセルするようにした
   * ドラッグ操作でタブを選択または閉じようとする時の挙動を、エクスプローラ上でのファイル選択や文字列の範囲選択の挙動と同様にした（今までは単にタブの上をポインタが通過しただけで選択の状態を切り替えていた）
   * 「左（上）のタブを閉じる」でピン留めされたタブを閉じないようにした
   * Panoramaで他のグループにタブがある時に、メニューの「右（下）のタブを閉じる」「左（上）のタブを閉じる」が意図せず無効になってしまう場合があったのを修正
   * ru-RUロケール更新（by Netanyahu）
 - 0.6.2011082901
   * 註：このバージョンおよびこれ以前のバージョンは、[bug 455694](https://bugzilla.mozilla.org/show_bug.cgi?id=455694)および[bug 674925](https://bugzilla.mozilla.org/show_bug.cgi?id=674925)の影響によりFirefox 8以降には非対応です
   * 現在のタブの暗黙的な選択に関する挙動をカスタマイズできるようにした
   * 複数のタブを閉じる時の警告を "extensions.multipletab.warnOnCloseMultipleTabs" でカスタマイズできるようにした（ `-1` ="browser.tabs.warnOnClose"を使用,  `0` =警告しない,  `1` =警告する)
   * Metaタグの情報を使用するための以下の新しいプレースホルダに対応： `%AUTHOR%` ,  `%AUTHOR_HTMLIFIED%` ,  `%DESCRIPTION%` ,  `%DESCRIPTION_HTMLIFIED%` ,  `%KEYWORDS%` ,  `%KEYWORDS_HTMLIFIED%` 
   * タブが1つだけ選択されている時にドラッグできない問題を修正
   * 素早くタブを選択した時にいくつかのタブが選択されない問題を修正（Thanks titoBouzout!）
   * コンテンツ領域のコンテキストメニューが表示されなくなる問題を修正
   * 日本語ロケールにおいてタブ選択時のメニューのラベル文字列を短くした
   * ru-RUロケール更新（by Netanyahu）
 - 0.6.2011051101
   * タブ上でのCtrl（Command）-クリックに対してマルチプルタブハンドラ自身が何もしないよう明示的に設定できるようにした
   * ピン留めされたタブを「他のタブを閉じる」で閉じないようにした
   * 現在のタブの上でのCtrl（Command）-クリックでそのタブ自身が選択されない問題を修正
   * Firefox 4において、タブバー上に配置されたツールバー項目の上へのタブのドロップが機能していなかったのを修正
   * [Locationbar2](https://addons.mozilla.org/firefox/addon/locationbar%C2%B2/)と併用できるようにした
   * [Personal Titlebar](https://addons.mozilla.org/firefox/addon/personal-titlebar/)との併用時に初期化処理が2回呼ばれてしまっていたのを修正
   * Tab Mix Plusとの併用時のTabDNDObserverに関する互換性の問題を解消
   * フランス語ロケール追加（translated by Jean-Philippe Fleury）
   * 簡体中国語ロケール更新（translated by hzhbest）
 - 0.6.2011020301
   * Tab Mix Plusがあるとタブをドラッグ＆ドロップできなくなる問題に対処
   * [Personal Titlebar](https://addons.mozilla.org/firefox/addon/personal-titlebar/)との併用を可能にした
   * [DragNDrop Toolbars](https://addons.mozilla.org/firefox/addon/dragndrop-toolbars/)との併用を可能にした
 - 0.6.2011011701
   * Minefieldにおいて、選択したタブに対して「タブをピン留めする」「タブのピン留めを外す」「グループへ移動」を実行できるようにした
   * Minefieldにおいて、Panoramaを開く前にタブの選択状態を解除するようにした
 - 0.6.2011011102
   * DOMイベントを使用したAPIについて、旧来のイベント名（nsDOMというプレフィクスが付かない物）でも `getData()` で情報を取得できるようにした
 - 0.6.2011011101
   * タブが選択されてからマウスのボタンが放されるまでの間に時間がかかってしまった場合に、意図しないポップアップが表示されないように修正
   * 複数のタブをまとめて閉じる機能について、閉じられるタブとして選択中のタブのクローズボックスの表示スタイルをより目立たないように変更
   * DOMイベントを使用したAPIについて、Minefieldでのセキュリティ上の制約により、「nsDOM」プレフィクス付きのイベント名で、DataContainerEventとしてイベントを送出するように仕様を変更（後方互換性のため過去のプロパティアクセス表記も利用可能ですが、Firefox 4以降では、場面によってはセキュリティ上の制限からプロパティアクセスを利用できません。安全のため、今後は  `aEvent.getData(プロパティ名)`  でプロパティの内容を参照するようにしてください。）
 - 0.6.2010121701
   * 同じサイトのタブを閉じる機能について、別のユーザのホームに属しているURI（ /~username/ の部分が異なる場合）は別のサイトと見なすようにした（ extensions.multipletab.checkUserHome=false で従来の動作）
   * multipletab-selected属性の代わりにmultiselected属性を使用するようにした（互換性のため、以前の属性名も使用されます）
   * Tab Mix Plusがあるとタブをドラッグ＆ドロップできなくなる問題に対処
   * ru-RUロケールの一部を前バージョンの内容に差し戻した
 - 0.6.2010120202
   * 複数のタブをブックマークサイドバー等にドロップした際にすべてのタブをブックマークする機能が働かなくなっていたのを修正
   * Minefieldにおいて読み込みが完了していないタブをブックマークできるようにした
 - 0.6.2010120201
   * Windows上のFirefox 3.6以前では複数タブのドラッグ時にカーソルの形を変えないようにした（ドラッグ操作のフィードバック用画像が表示されないバグのため）
   * クローズボックスのドラッグによって選択されている状態のタブについて、クローズボックスの強調表示のスタイルを修正
 - 0.6.2010120101
   * Firefox 3.0系のサポートを終了
   * HTML5のドラッグ＆ドロップのAPIに基づく実装に変更し、複数のタブをドラッグするときはそれらをdata transferに渡すようにした
   * 複数のタブに対するドラッグ＆ドロップの動作を始める前に「MultipleTabHandler:TabsDragStart」イベントを発行するようにした（このイベントをpreventDefault()でキャンセルすることで、複数タブのドラッグ＆ドロップ時の挙動を任意の挙動に変更できます）
   * Menu Editorの設定ダイアログの呼び出しに失敗していたのを修正
   * クローズボックスのドラッグによって選択されている状態のタブについて、クローズボックスの強調表示をより強く行うようにした
 - 0.5.2010111401
   * Minefieldでのタブの仕様変更に追従
   * Minefieldでセッションが復元されない問題を修正
 - 0.5.2010070301
   * Minefield 4.0b2preで他のアドオンの状態に応じた設定項目の有効・無効の切り替えが行われない問題を修正
   * 0.5.2010062901のリグレッション：ツリー型タブが無いと動作しなくなっていたのを修正
 - 0.5.2010062901
   * Minefield 3.7a6preでタブバー上でのドラッグ中の自動スクロールが効かなくなっていたのを修正
   * ロシア語ロケール更新（by L'Autour）
 - 0.5.2010043001
   * バックグラウンドにあるタブをクリックして、タブがフォアグラウンドになるまでに時間がかかってしまった場合に、タブを選択しようとしているわけでもないのにタブが選択されてしまう現象を起こらないようにした。
   * multipletab-available属性のみが指定されていてextensions.multipletab.show.*の設定値が存在しない場合に、メニュー項目の表示・非表示の切り替えが期待通りに行われない問題を修正
 - 0.5.2010040201
   * [Bug 554991  - allow tab context menu to be modified by normal XUL overlays](https://bugzilla.mozilla.org/show_bug.cgi?id=554991)による仕様変更に追従
 - 0.5.2010032901
   * es-ESロケールが壊れていたのを修正
 - 0.5.2010032801
   * Minefield 3.7a4pre対応
   * 選択したタブをブックマークサイドバーへドラッグ＆ドロップした時に、まとめてブックマークする機能が働いていなかったのを修正
   * [BarTab](https://addons.mozilla.org/firefox/addon/67651)によって待機状態にされているタブについて、なるべく正しくURIを取得できるようにした
   * es-ESロケール更新（by tito）
   * ru-RUロケール更新（by Netanyahu）
   * it-ITロケール更新（by Godai71）
 - 0.5.2010020801
   * 「似たタブを閉じる」機能について、選択中のタブも閉じるようにした
   * これまでのバージョンでの「似たタブを閉じる」機能と同じ結果になる「他の似たタブを閉じる」を追加
   * 選択したタブをまとめて保存する機能が働かなくなっていたのを修正
   * [BarTap](https://addons.mozilla.org/firefox/addon/67651)との連携がうまくいっていなかったのを修正
 - 0.5.2010020301
   * [BarTap](https://addons.mozilla.org/firefox/addon/67651)によって読み込みが中断されているタブについては、操作を行う前にタブの読み込みを行うようにした
   * Firefox 3.6以降で、開き直せない状態にしてからタブを閉じる処理が期待通りに動いていなかったのを修正
   * zh-CNロケール更新（by hzhbest）
   * ru-RU ロケール更新（by Netanyahu）
 - 0.5.2010012001
   * 複数のタブをまとめて閉じた後に、[Echofon](https://addons.mozilla.org/firefox/addon/5081)などによる常時表示型のパネルが消えてしまう問題に対処
   * [ツリー型タブ](http://piro.sakura.ne.jp/xul/_treestyletab.html)と組み合わせた時に、ブックマークを並べ替えようとするとエラーになる問題を修正
   * [Super Tab Mode](https://addons.mozilla.org/firefox/addon/13288)がインストールされている環境で、選択されたタブに対して「タブのロック」を行えるようにした
   * [Tab Utilities](https://addons.mozilla.org/firefox/addon/59961)がインストールされている環境で、選択したタブのロック・保護・凍結の各メニューの表示・非表示を任意に設定できるようにした
   * it-ITロケール更新（by Godai71）
   * hu-HUロケール更新（by Mikes Kaszmán István）
 - 0.5.2010011601
   * 複数のタブをブックマークフォルダ上にドロップした時に、その位置に複数のブックマーク項目を同時に生成するようにした
   * タブをShift-クリックした時の挙動を変更できるようにした
   * Tab Mix Plusがインストールされている場合、タブの上でのCtrl-クリックとShift-クリックをどちらのアドオンの操作に使うかを訊ねるようにした
   * タブのURIをコピーする際、タイトルやURIの一部に「$1」が含まれているとその部分が意図せず置き換えられてしまう問題を修正
   * ツリー型タブで親のタブを選択した時、実際には折りたたまれていないツリーが全選択されてしまうことがあったのを修正
   * 複数のタブをまとめて閉じる直前に `MultipleTabHandlerTabsClosing` イベント、閉じた直後に `MultipleTabHandlerTabsClosed` イベントを発行するようにした
   * [Undo Tab Operations](https://addons.mozilla.org/firefox/addon/58033/)との併用で複数のタブへの操作をやり直せるようにした
   * de-DEロケール追加（by mpeters and saskia_br）
   * pl-PLロケール追加（by Jacek Chrząszcz）
   * ru-RU ロケール更新（by Netanyahu）
   * it-ITロケール更新（by Godai71）
 - 0.5.2009110501
   * Minefield, Firefox 3.6対応
   * Firefox 2のサポートを終了
   * より安全なコードへ
   * 実際のタブの状態と保存されたセッション情報との間に不整合が発生する可能性があったのを修正
   * ツリー型タブでインデントされたタブについて、インデント部分の余白の上ではmousemoveイベントを拾わないようにした
 - 0.4.2009073101
   * 選択したタブをブックマークに保存する際、[ツリー型タブ](http://piro.sakura.ne.jp/xul/_treestyletab.html)のツリー構造を含めるようにした
   * Tab Mix Plusがある時、ブックマークの保存に失敗する問題を修正
   * hu-HUロケール更新（by Mikes Kaszmán István）
 - 0.4.2009072001
   * タブのURIをコピーする時の形式を自由に追加できるようにした（[Copy URL+](https://addons.mozilla.org/firefox/addon/129)互換）
 - 0.3.2009071601
   * Tab Mix Plusがインストールされている環境で、選択したタブに対して「タブをロック」「タブを保護」「タブを凍結」を実行できるようにした
   * Tab Mix Plusでタブバーが複数行で表示されている時、タブのドラッグによる選択が機能しない問題を修正
   * Tab Mix Plusでタブバーが複数行で表示されている時、タブのドラッグ中は縦方向にオートスクロールするようにした
   * Firefox 3.5で、すべてのタブをドラッグした時の除外処理が働いていなかったのを修正
   * zh-CNロケール追加（by hzhbest）
 - 0.3.2009062901
   * ウィンドウをまたいでタブを移動した後に、移動されたタブを選択したままにするかどうかの設定が、Firefox 3.0では無視されていたのを修正
   * Firefox 3.5 on Mac OS XでタブのThrobberが表示されなくなる問題に対処
   * イタリア語ロケール更新（by Godai71）
   * 台湾中国語ロケール更新（by Tsprajna）
   * ハンガリー語ロケール更新（by Mikes Kaszmán István）
 - 0.3.2009062301
   * 複数のタブをまとめて閉じる時、閉じるタブの数を正しく表示するようにした
   * 複数のタブをまとめて閉じる時について、タブを閉じる順番を設定できるようにした
   * タブの複製とウィンドウをまたいだタブの移動について、自動的にタブを選択するかどうか設定できるようにした
   * it-ITロケールの更新ミスがあったのを修正
 - 0.3.2009051501
   * hu-HUロケール更新（by Mikes Kaszmán István）
 - 0.3.2009051301
   * [Menu Editor](https://addons.mozilla.org/firefox/addon/710)と連携して動作するようにした（タブ選択時のメニューをカスタマイズできるようにし、マルチプルタブハンドラの設定ダイアログからMenu Editorの設定ダイアログを開けるようにした）
   * APIによるタブのコンテキストメニューへのメニュー項目の追加時に、項目の位置の指定方法として `multipletab-insertbefore` に加えて `multipletab-insertafter` も利用できるようにした
   * APIによるタブのコンテキストメニューへのメニュー項目の追加時に、 `multipletab-insertbefore` と `multipletab-insertafter` でXPath式を利用できるようにした
   * タブのコンテキストメニューに挿入する項目の並び順を変更した
   * 他のアドオンがAPIを使ってタブのコンテキストメニューに挿入する項目より先に、マルチプルタブハンドラ自身が提供する項目を挿入するようにした
 - 0.3.2009051101
   * クリップボードにコピーする文字列の改行コードをプラットフォームに合わせて変えるようにした（WindowsではCR+LF、LinuxおよびMac OS XではLF）
   * タブを複製した後に再度タブの複製を実行すると、タブが2重に複製されてしまう問題を修正
   * zh-TWロケール更新（by Tsprajna）
 - 0.3.2009043002
   * Minefieldで動作しなくなっていたのを修正
 - 0.3.2009043001
   * [分割ブラウザ](http://piro.sakura.ne.jp/xul/_splitbrowser.html)で、他のペインが存在するときにメインのブラウズ領域の最後のタブを別のウィンドウに移動した場合、ウィンドウを閉じないようにした
 - 0.3.2009042901
   * タブの選択時のメニューに「他をすべて閉じる」を追加
   * Effective TLDに基づいて、サブドメインが異なるページを開いているタブも「似たタブ」として認識するようにした（Firefox 3以降のみ）
   * 選択したタブのURIをHTMLとしてコピーする時、URIやタイトルの中に含まれる特殊文字をエンティティ参照に置換するようにした
   * コンテキストメニューなどから「タブを複製」を実行するとすべてのタブが選択されてしまっていたのを修正
   * zh-TWロケール追加（translated by Tsprajna）
 - 0.3.2009040901
   * タブの選択などのドラッグ中にタブバーを自動スクロールするようにした
 - 0.3.2009040201
   * Minefieldで動作しなくなっていたのを修正
 - 0.3.2009032501
   * 選択されたタブの強調表示スタイルを、他のアドオンでのスタイル指定よりも優先的に適用するようにした
 - 0.3.2009021201
   * 内部処理を改善
 - 0.3.2008122801
   * タブバー上のボタンやスクロールバーなどでの上でのクリック操作ではタブの選択を解除しないようにした
   * ルーマニア語ロケール追加（by L'Autour）
   * イタリア語ロケール更新（by Godai71）
 - 0.3.2008120401
   * [Print All Tabs](https://addons.mozilla.org/firefox/addon/5142)がインストールされている場合、選択されたタブをメニューから印刷できるようにした
   * [ツリー型タブ](http://piro.sakura.ne.jp/xul/_treestyletab.html)がインストールされている場合、タブのインデント部分でもタブの選択を開始できるようにした
   * ハンガリー語ロケール更新（by Mikes Kaszmán István）
 - 0.3.2008120201
   * 選択したタブをまとめてダウンロードする機能を追加
   * タブの上でボタンを押下しっぱなしにした時に、最初のタブが自動的に選択されていなかったのを修正
   * Minefield 3.1b3preで、選択されたタブをウィンドウ外にドロップして新しいウィンドウに分離できるようにした
 - 0.3.2008111401
   * 選択されたモードに応じて設定ダイアログ内の無用なチェックボックスを自動的に無効化するようにした
   * イタリア語ロケール更新（by Godai71）
   * スペイン語ロケール更新（by tito）
   * ハンガリー語ロケール更新（by Mikes Kaszmán István）
 - 0.3.2008101801
   * タブをドラッグで選択した後にポップアップメニューを自動的に開かない設定を加えた
   * メニュー項目の表示カスタマイズ用チェックボックスのリストを設定ダイアログの大きさいっぱいまで広げて表示するようにした
 - 0.3.2008101701
   * Minefield 3.1b2preで、ウィンドウ間で複数のタブを移動する時に、内容の再読み込み無しでタブを移動するようにした
   * Minefield 3.1b2preで、選択されたタブを新しいウィンドウで開く時に、内容の再読み込み無しでタブを移動するようにした
   * 違うウィンドウに複数のタブをドロップする時、Ctrlキー（Commandキー）を押している場合は複製、そうでない場合は移動するようにした
   * メニュー項目が重複して表示されたままになる問題を修正
 - 0.2.2008101501
   * タブのクローズボックスをドラッグしてタブをまとめて閉じる時、[ツリー型タブ](http://piro.sakura.ne.jp/xul/_treestyletab.html)で折りたたまれたタブを消し残すことがあったのを修正
   * [Menu Edit](https://addons.mozilla.org/firefox/addon/710)で項目が無限増殖する問題に対処
   * Tab Mix Plusがインストールされていると選択されたタブをブックマークできなくなる問題を修正
   * 「左のタブを閉じる」「右のタブを閉じる」について、該当するタブがない時は項目を無効化するようにした
   * タブが一つしかない時は「全てのタブを…」系の項目を隠すようにした
 - 0.2.2008050601
   * イタリア語ロケール更新
 - 0.2.2008050201
   * Firefox 3で選択したタブをまとめてブックマークできなくなっていたのを修正
 - 0.2.2008040701
   * タブを複製した後は、複製されたタブを必ず選択するようにした
   * Firefox 3での外観を調整
 - 0.2.2008031001
   * タブの複製に失敗する問題を修正
   * タブ選択時のメニューでサブメニューが閉じられると選択が解除されてしまう問題を修正
   * スペイン語ロケール追加（by tito, Thanks!）
   * Minefield 3.0b5preでの動作を確認
 - 0.2.2008022801
   * [Tab Groups](http://paranoid-androids.com/tabgroups/)と同時に利用するとタブの複製や別ウィンドウへの移動が正常に行えなくなる問題を修正
 - 0.2.2008022701
   * [Linkwad](https://addons.mozilla.org/ja/firefox/addon/3263)、[Tab Groups](http://paranoid-androids.com/tabgroups/)においてグループの間で複数のタブをドラッグ＆ドロップで移動できるようにした
 - 0.2.2008022502
   * 複数タブをドラッグ＆ドロップした時にドロップ位置のインジケータが消えずに残ることがある問題を修正
   * 複数タブをドラッグ＆ドロップして移動または複製する時に、ドラッグ前と同じ並び順になるようにした
 - 0.2.2008022501
   * ハンガリー語ロケール更新（by Mikes Kaszmán István）
 - 0.2.2008022402
   * Firefox 3において、選択された複数のタブをまとめてドラッグ＆ドロップで複製および他のウィンドウに移動できるようにした
   * Firefox 3において、タブの選択状態が表示されない問題を修正
 - 0.2.2008022401
   * 選択された複数のタブをまとめてドラッグ＆ドロップで移動できるようにした
   * duplicateTabメソッドをgBrowserに追加するようにした
 - 0.2.2007111801
   * [ツリー型タブ](http://piro.sakura.ne.jp/xul/_treestyletab.html)と併用した時、サブツリーが折り畳まれたタブを選択した時は折り畳まれたタブもすべて選択するようにした
 - 0.2.2007111301
   * Tab Mix Plusと併用した時にタブのクローズボックスのドラッグでタブをまとめて閉じる機能が働かない問題を修正
 - 0.2.2007110601
   * ドラッグでのタブの選択が開始される前にボタンを放した場合、選択を解除して、ポップアップメニューも表示しないようにした
   * ドラッグでのタブ切り替え操作について遅延が機能していなかったのを修正
   * ドラッグでの選択/タブ切り替え操作について、初期状態で遅延を設定した
 - 0.2.2007110501
   * タブのURIをコピーする際、形式をメニューから選択できるようにした
   * タブのドラッグで選択を開始またはタブを切り替える設定について、操作を有効にするまでの遅延時間を設定できるようにした
   * イタリア語ロケール追加（by Godai71.Extenzilla）
 - 0.1.2007103101
   * [ImgLikeOpera](https://addons.mozilla.org/firefox/addon/1672)、[Session Fix](https://addons.mozilla.org/firefox/addon/4542)との衝突を解消
   * [ColorfulTabs](https://addons.mozilla.org/firefox/addon/1368)または[ChromaTabs](https://addons.mozilla.org/firefox/addon/3810)が有効な環境では、選択されたタブの強調表示を枠線で行うようにした
 - 0.1.2007102501
   * Minefieldにおいて、選択したタブをブックマークフォルダに保存する機能が働くようにした
 - 0.1.2007061801
   * 複数タブ選択時のポップアップメニューやタブのコンテキストメニューで無用なセパレータが表示されたままになることがあったのを修正
   * 英語ロケールのミスを修正
 - 0.1.2007060601
   * 「URIをコピー」「似たタブを閉じる」機能を追加
   * ハンガリー語ロケールを更新
 - 0.1.2007050701
   * タブをドラッグで移動する設定の時、favicon以外に反応していなかったのを修正
   * 日本語ロケールのミスを修正
 - 0.1.2007050601
   * いくつかのAPIについて、動作に不備があったのを修正
 - 0.1.2007042601
   * ポップアップがずれて表示される問題を修正
 - 0.1.2007042501
   * [All-in-One Gestures](https://addons.mozilla.org/firefox/addon/12)との競合を解消
 - 0.1.2007042003
   * 「タブを複製」機能を追加
   * ウィンドウを分割する処理の効率を改善
 - 0.1.2007042002
   * アイコンを追加
   * 「すべてのタブを閉じる」機能を追加
   * 選択されたタブをブックマークする機能を追加
   * タブの再読み込みでまで確認が出てしまっていたのを修正
 - 0.1.2007042001
   * 公開
