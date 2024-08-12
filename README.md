
## 概要
・chrome devloper tool を使い twig のtemplate suggestions を頼りにしながら
作成した。

## 工夫した点
・動的なpageであるため静的なpageのように要素がどこのファイルにあり、分かりにくかった。
そのため実際にオーバーライドしたtemplatesを変更し、classに値を当てはめてどこのコードが
どこに対応するのか確認しながら作成した。

・コードの記述を間違えて画面上にエラーが出ると、上部のtoolbarまでもが表示されなくなってしまい
キャッシュクリアできなくなってしまう。そのためdrushをインストールしてcli上でdrush crすることによって対応した。

・特にblock--system-branding-block.html.twigなどの編集は難しく、drupalによって
出力されるコンテンツの中身がpタグによって動的に生成されるので,wrapperのdivタグで囲い
ブロック要素限定の操作を行えるようにした。