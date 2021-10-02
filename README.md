# nissya_utf8

このファイルは樋󠄀口耕一さんが[LaTeX tiny Tips](http://koichi.nihon.to/psnl/latex0.html#nissya)で公開してくださっているnissya.bstに手直しを加え、姓, 名 の形式で書かれた日本語文献を含むbibファイルからそれらしい出力を得られるようにしたものです。

# 基本的な更新箇所

- 姓, 名の順でかかれた日本語文献を含むbibフィアルを利用できるようなりました。
- 2018年に改定された社会学評論のスタイルガイドにあわせて邦訳外国語文献を参考文献に挙げる際の ＝ を取り除きました。

# 使い方

- 基本的には樋󠄀口耕一さんが公開している[PDF](http://koichi.nihon.to/psnl/tex/nissya_bib.pdf)の記述と同様にお使いいただけるはずです。プリアンブルに\usepackage{nissya_bib_utf8}、文書内に\bibliography{お使いのbibファイル名}を書いておいてください。
- コンパイルはLuaLaTeX - upBibTeX - LuaLaTeX×2です。
- 樋󠄀口耕一さんが公開しているsample.texをLuaLaTeXで走るように更新したsample_uft.texを同梱していますので、あわせてご参照ください。

## 基本的な挙動

- \citet, \citepなどは変わらず使えます。
- 初出はフルネーム、2回目以降は名字orラストネームで出力されるはずです。
- 著者、編者が3人以上の場合、 ほか or et al. で省略されるはずです。
- bibファイルのlanguageフィールドで言語を指定し(en or jp)、邦文文献のyomiフィールドに著者名をひらがなで入れてやると、五十音順に並ぶことを確認しています。yomiフィールドも姓, 名の順で記述してください。

# ご注意

- bstの編集は初めての挑戦です。各サイトの情報を見ながら編集とコンパイルを繰り返し、理想的な出力を探り当てたような感じなので、汚い編集が盛りだくさんになっているかと思います･･･。変な挙動があればどんどん手直ししてくださるとありがたいです。
- 私の環境(LuaLaTeX+upBibTeX)では一応動いていますが、他の環境での動作は保証できません。
- 社会学評論によせてはいますが、対応できていない部分もたくさんあると思います。
- できたてホヤホヤなので使っていくうちにボロが出てくると思います。
- これらのファイルをご利用になったことで生じたいかなる不利益についても筆者は責任を負いかねます。

# その他

- おそらく、このファイルを使うメリットは翻訳書・翻訳論文を挙げる際に社会学評論が求める、 著者名(原著の出版年=訳本の出版年)というスタイルが必要な場合に限られると思います。単にAuthor-year形式の出力が必要なのであればjecon.bstがおすすめです。


# ライセンス

樋󠄀口耕一さんが公開してくださっているnissya.bstは飯田修さんによって作成されたjpolisci.bstを武田史郎さんが経済学用に書き換えたjecon.bstを編集したものとのことです。“LaTeX Project Public License”に準拠しいるつもりでいるので以下の条件を守りつつ、自由に複製、変更、配布していただいて結構です。
 
(1) you make absolutely no changes to your copy, including name, or

(2) if you do make changes, you name it something other than,
　　 natbib.sty, jbtxbst.doc, jplain.bst, junsrt.bst, jalpha.bst, jabbrv.bst, tipsj.bst, jipsj.bst, tieice.bst, jname.bst, jorsj.bst, jglsj.bst, seg.bst, jpolisci.bst, jecon.bst, nissya.bst, nissyal.bst, nissya_bib.sty, nissya_utf8.bst, nissyal_utf8.bst, nissya_bib_uft8.sty
