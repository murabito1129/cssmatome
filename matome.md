1. [CSS入門の自分用まとめ（参考：とほほのCSS入門、というか写し）](#css入門の自分用まとめ参考とほほのcss入門というか写し)
   1. [基本セレクタ](#基本セレクタ)
      1. [tagname{...}](#tagname)
      2. [.class{...}](#class)
      3. [#id{...}](#id)
      4. [\*{...}](#)
      5. [namespace | E](#namespace--e)
   2. [属性セレクタ](#属性セレクタ)
      1. [\[attr\]](#attr)
      2. [\[attr=value\]](#attrvalue)
      3. [\[attr~=value\]](#attrvalue-1)
      4. [\[attr|=value\]](#attrvalue-2)
      5. [\[attr^=value\]](#attrvalue-3)
      6. [\[attr$=value\]](#attrvalue-4)
      7. [\[attr\*=value\]](#attrvalue-5)
      8. [\[ns|attr\]](#nsattr)
   3. [結合子](#結合子)
      1. [E,F,...{...}](#ef)
      2. [E F ...{...}](#e-f-)
      3. [E \> F](#e--f)
      4. [E+F](#ef-1)
      5. [E ~ F {...}](#e--f-)
   4. [疑似クラス](#疑似クラス)
      1. [入力疑似クラス](#入力疑似クラス)
         1. [:autofill](#autofill)
         2. [:enabled](#enabled)
         3. [:disabled](#disabled)
         4. [:read-only](#read-only)
         5. [:read-write](#read-write)
         6. [:placeholder-shown](#placeholder-shown)
         7. [:default](#default)
         8. [:indeterminate](#indeterminate)
         9. [:blank](#blank)
         10. [:valid](#valid)
         11. [:invalid](#invalid)
         12. [:in-range](#in-range)
         13. [:out-of-range](#out-of-range)
         14. [:required](#required)
         15. [:optional](#optional)
      2. [言語疑似クラス](#言語疑似クラス)
         1. [:lang(c)](#langc)
      3. [位置疑似クラス](#位置疑似クラス)
         1. [:link](#link)
         2. [:visited](#visited)
         3. [:target](#target)
      4. [リソース状態疑似クラス](#リソース状態疑似クラス)
      5. [ツリー構造疑似クラス](#ツリー構造疑似クラス)
         1. [:root](#root)
         2. [:empty](#empty)
         3. [:nth-child(n)](#nth-childn)
         4. [: nth-last-child(n)](#-nth-last-childn)
         5. [:first-child](#first-child)
         6. [:last-child](#last-child)
         7. [:only-child](#only-child)
         8. [:nth-of-type(n)](#nth-of-typen)
         9. [:nth-last-of-type(n)](#nth-last-of-typen)
         10. [:first-of-type](#first-of-type)
         11. [:last-of-type](#last-of-type)
         12. [:only-of-type](#only-of-type)
      6. [ユーザー操作疑似クラス](#ユーザー操作疑似クラス)
         1. [:hover](#hover)
         2. [:active](#active)
         3. [:focus](#focus)
         4. [:focus-visible](#focus-visible)
      7. [論理結合疑似クラス](#論理結合疑似クラス)
         1. [:is(...) , where(...)](#is--where)
         2. [:not(...)](#not)
      8. [表示状態疑似クラス](#表示状態疑似クラス)
         1. [:open](#open)
         2. [:fullscreen](#fullscreen)
         3. [:modal](#modal)
         4. [:picture-in-picture](#picture-in-picture)
      9. [その他疑似クラス](#その他疑似クラス)
         1. [:defined](#defined)
   5. [擬似要素](#擬似要素)
      1. [タイポグラフィック擬似要素](#タイポグラフィック擬似要素)
         1. [::first-line](#first-line)
         2. [::first-letter](#first-letter)
      2. [ハイライト擬似要素](#ハイライト擬似要素)
         1. [::selection](#selection)
      3. [ツリー永続系](#ツリー永続系)
         1. [::before](#before)
         2. [::after](#after)
         3. [::marker](#marker)
         4. [::placeholder](#placeholder)
         5. [::backdrop](#backdrop)
   6. [ルール](#ルール)
      1. [基本ルール](#基本ルール)
         1. [@charset](#charset)
         2. [@import](#import)
      2. [フォントルール](#フォントルール)
         1. [@font-face](#font-face)
      3. [レイアウト・メディアルール](#レイアウトメディアルール)
         1. [@media](#media)
         2. [@keyframes](#keyframes)
   7. [宣言](#宣言)
      1. [!important](#important)
   8. [値](#値)
      1. ['number'](#number)
      2. ['integer'](#integer)
      3. ['length'](#length)
      4. ['percemtage'](#percemtage)
      5. ['string'](#string)
      6. ['angle'](#angle)
      7. ['color'](#color)
      8. ['image'](#image)
      9. ['position'](#position)
      10. ['frequency'](#frequency)
      11. ['time'](#time)
      12. ['url'](#url)
      13. ['cursom-ident'](#cursom-ident)
      14. ['initial , revert , inherit , unsert'](#initial--revert--inherit--unsert)
   9. [参照関数](#参照関数)
      1. [var()](#var)
      2. [url()](#url-1)
   10. [計算関数](#計算関数)
       1. [calc()](#calc)
   11. [比較関数](#比較関数)
       1. [min()](#min)
       2. [max()](#max)
       3. [clamp()](#clamp)
   12. [段階値関数](#段階値関数)
   13. [数学関数](#数学関数)
   14. [描画関数](#描画関数)
       1. [image-set()](#image-set)
   15. [プロパティ](#プロパティ)
       1. [全プロパティ](#全プロパティ)
          1. [all](#all)
       2. [色系プロパティ](#色系プロパティ)
          1. [color](#color-1)
          2. [accent-color](#accent-color)
          3. [color-scheme](#color-scheme)
          4. [opacity](#opacity)
          5. [rgb/rgba](#rgbrgba)
          6. [forced-color-adjust](#forced-color-adjust)
       3. [グラデーション系プロパティ](#グラデーション系プロパティ)
          1. [linear-gradient()](#linear-gradient)
          2. [radial-gradient()](#radial-gradient)
          3. [conic-gradient()](#conic-gradient)
          4. [repeating-linear-gradient()](#repeating-linear-gradient)
          5. [repeating-radial-gradient()](#repeating-radial-gradient)
          6. [repeating-conic-gradient()](#repeating-conic-gradient)
       4. [フォント系プロパティ](#フォント系プロパティ)
          1. [font](#font)
          2. [font-style](#font-style)
          3. [font-weight](#font-weight)
          4. [font-size](#font-size)
          5. [font-family](#font-family)
          6. [font-stretch](#font-stretch)
          7. [font-synthesis](#font-synthesis)
          8. [font-synthesis-style](#font-synthesis-style)
          9. [font-synthesis-weight](#font-synthesis-weight)
          10. [font-synthesis-small-caps](#font-synthesis-small-caps)
          11. [font-kerning](#font-kerning)
          12. [font-variant-numeric](#font-variant-numeric)
          13. [font-variant-caps](#font-variant-caps)
          14. [font-variant-ligatures](#font-variant-ligatures)
          15. [font-variant-east-asian](#font-variant-east-asian)
          16. [font-optical-sizing](#font-optical-sizing)
       5. [テキスト系プロパティ](#テキスト系プロパティ)
          1. [text-indent](#text-indent)
          2. [text-align](#text-align)
          3. [vertical-align](#vertical-align)
          4. [text-transform](#text-transform)
          5. [line-height](#line-height)
          6. [word-spacing](#word-spacing)
          7. [letter-spacing](#letter-spacing)
          8. [user-select](#user-select)
       6. [改行系プロパティ](#改行系プロパティ)
          1. [white-space](#white-space)
          2. [word-break](#word-break)
          3. [overflow-wrap](#overflow-wrap)
          4. [hyphens](#hyphens)
       7. [テキストデコレーション系プロパティ](#テキストデコレーション系プロパティ)
          1. [text-shadow](#text-shadow)
          2. [text-decoration(-style/-color)](#text-decoration-style-color)
          3. [text-decoration-skip-ink](#text-decoration-skip-ink)
          4. [text-decoration-thickness](#text-decoration-thickness)
          5. [text-emphasis(-style/-color)](#text-emphasis-style-color)
       8. [文章方向系プロパティ](#文章方向系プロパティ)
          1. [writing-mode](#writing-mode)
          2. [text-orientation](#text-orientation)
       9. [ルビ系プロパティ](#ルビ系プロパティ)
          1. [ruby-position](#ruby-position)
       10. [改ページ・改カラム系プロパティ](#改ページ改カラム系プロパティ)
           1. [break-before/-after/-inside](#break-before-after-inside)
           2. [box-decoration-break](#box-decoration-break)
       11. [リスト系プロパティ](#リスト系プロパティ)
           1. [list-style(-type,-position,-image)](#list-style-type-position-image)
       12. [カウンター系プロパティ](#カウンター系プロパティ)
           1. [counter-set](#counter-set)
           2. [counter-set　](#counter-set-1)
           3. [counter-reset](#counter-reset)
           4. [counter-increment](#counter-increment)
           5. [counter()/counters()](#countercounters)
       13. [テーブル系プロパティ](#テーブル系プロパティ)
           1. [caption-side](#caption-side)
           2. [table-layout](#table-layout)
           3. [border-collapse(-spacing)](#border-collapse-spacing)
           4. [empty-cells](#empty-cells)
       14. [コンテント作成系プロパティ](#コンテント作成系プロパティ)
           1. [content](#content)
       15. [印刷系プロパティ](#印刷系プロパティ)
           1. [size](#size)
           2. [orphans/widows](#orphanswidows)
       16. [ブレンド系プロパティ](#ブレンド系プロパティ)
           1. [mix-blend-mode](#mix-blend-mode)
           2. [background-blend-mode](#background-blend-mode)
       17. [配置系プロパティ](#配置系プロパティ)
           1. [position](#position-1)
           2. [top/right/bottom/left](#toprightbottomleft)
           3. [inset](#inset)
           4. [z-index](#z-index)
       18. [表示系プロパティ](#表示系プロパティ)
           1. [float](#float)
           2. [clear](#clear)
           3. [overflow(-x/-y)](#overflow-x-y)
           4. [overflow-clip-margin](#overflow-clip-margin)
           5. [text-overflow](#text-overflow)
           6. [visibility](#visibility)
           7. [display](#display)
           8. [appearance](#appearance)
           9. [contain](#contain)
       19. [margin系プロパティ](#margin系プロパティ)
           1. [margin(-top/-right/-bottom/-left)](#margin-top-right-bottom-left)
           2. [padding系プロパティ](#padding系プロパティ)
           3. [padding(-top/-right/-bottom/-left)](#padding-top-right-bottom-left)
       20. [サイズ系プロパティ](#サイズ系プロパティ)
           1. [width/height](#widthheight)
           2. [min-/max- width/hright](#min-max--widthhright)
           3. [box-sizing](#box-sizing)
           4. [resize](#resize)
           5. [aspect-ratio](#aspect-ratio)
       21. [背景系プロパティ](#背景系プロパティ)
           1. [background](#background)
           2. [background-color](#background-color)
           3. [background-image](#background-image)
           4. [background-repeat](#background-repeat)
           5. [background-attachment](#background-attachment)
           6. [background-position(-x/-y)](#background-position-x-y)
           7. [background-clip](#background-clip)
           8. [background-origin](#background-origin)
           9. [background-size](#background-size)
       22. [border系プロパティ](#border系プロパティ)
           1. [border(-top/-right/-bottom/-left) -(width/-style/-color)](#border-top-right-bottom-left--width-style-color)
           2. [border(-top-left/-top-right/-bottom-left/-bottom-right)-radius](#border-top-left-top-right-bottom-left-bottom-right-radius)
           3. [border-image](#border-image)
           4. [border-image-source](#border-image-source)
           5. [border-image-slice](#border-image-slice)
           6. [border-image-width](#border-image-width)
           7. [border-image-outset](#border-image-outset)
           8. [border-image-repeat](#border-image-repeat)
           9. [box-shadow](#box-shadow)
       23. [アウトライン系プロパティ](#アウトライン系プロパティ)
           1. [outline(-width/-style/-color)](#outline-width-style-color)
           2. [outline-offset](#outline-offset)
       24. [イメージ系プロパティ](#イメージ系プロパティ)
           1. [image-reading](#image-reading)
           2. [object-fit](#object-fit)
           3. [object-position](#object-position)
       25. [マスキング系プロパティ](#マスキング系プロパティ)
           1. [clip-path](#clip-path)
           2. [mask-image](#mask-image)
           3. [mask-size](#mask-size)
           4. [mask-repeat](#mask-repeat)
           5. [mask-position](#mask-position)
           6. [mask-origin](#mask-origin)
           7. [mask-clip](#mask-clip)
           8. [mask](#mask)
       26. [フィルタ系プロパティ](#フィルタ系プロパティ)
           1. [filter](#filter)
           2. [blur()](#blur)
           3. [brightness()](#brightness)
           4. [contrast()](#contrast)
           5. [drop-shadow()](#drop-shadow)
           6. [grayscale()](#grayscale)
           7. [hue-rotate()](#hue-rotate)
           8. [invert()](#invert)
           9. [opacity()](#opacity-1)
           10. [saturate()](#saturate)
           11. [sepia()](#sepia)
       27. [操作系プロパティ](#操作系プロパティ)
           1. [touch-action](#touch-action)
       28. [トランスフォーム系プロパティ](#トランスフォーム系プロパティ)
           1. [transform](#transform)
           2. [transform-origin](#transform-origin)
           3. [transform-style](#transform-style)
           4. [transform-box](#transform-box)
           5. [perspecgive](#perspecgive)
           6. [perspective-origin](#perspective-origin)
           7. [backface-visibility](#backface-visibility)
           8. [translate() / translateX/Y/Z/3d()](#translate--translatexyz3d)
           9. [scale() / scaleX/Y/Z/3d()](#scale--scalexyz3d)
           10. [rotate() / rotateX/Y/Z/3d()](#rotate--rotatexyz3d)
           11. [skew() / skewX/Y()](#skew--skewxy)
           12. [matrix()](#matrix)
           13. [matrix3d()](#matrix3d)
       29. [トランジション系プロパティ](#トランジション系プロパティ)
           1. [transition](#transition)
           2. [transition-property](#transition-property)
           3. [transition-duration](#transition-duration)
           4. [transition-timing-function](#transition-timing-function)
           5. [transition-delay](#transition-delay)
       30. [アニメーション系プロパティ](#アニメーション系プロパティ)
           1. [animation](#animation)
           2. [animation-name](#animation-name)
           3. [animation-duration](#animation-duration)
           4. [animation-timing-function](#animation-timing-function)
           5. [animation-delay](#animation-delay)
           6. [animation-iteration-count](#animation-iteration-count)
           7. [animation-direction](#animation-direction)
           8. [animation-fill-mode](#animation-fill-mode)
           9. [animation-play-state](#animation-play-state)
       31. [シェイプ系プロパティ](#シェイプ系プロパティ)
           1. [shape-outside](#shape-outside)
           2. [shape-margin](#shape-margin)
           3. [shape-image-threshold](#shape-image-threshold)
       32. [モーションパス系プロパティ](#モーションパス系プロパティ)
           1. [offset-path](#offset-path)
           2. [offset-distance](#offset-distance)
           3. [offset-position](#offset-position)
           4. [offset-rotate](#offset-rotate)
       33. [マルチカラム系プロパティ](#マルチカラム系プロパティ)
           1. [columns(-count/-width)](#columns-count-width)
           2. [column-rule(-color/-style/-width)](#column-rule-color-style-width)
           3. [column-span](#column-span)
           4. [colmn-fill](#colmn-fill)
       34. [フレックスボックス](#フレックスボックス)
           1. [flex-flow](#flex-flow)
           2. [flex-direction](#flex-direction)
           3. [flex-wrap](#flex-wrap)
           4. [order](#order)
           5. [flex](#flex)
           6. [flex-grow](#flex-grow)
           7. [flew-shrink](#flew-shrink)
           8. [flex-basis](#flex-basis)
       35. [グリッド](#グリッド)
           1. [grid](#grid)
           2. [grid-template](#grid-template)
           3. [grid-template-areas](#grid-template-areas)
           4. [grid-template-rows](#grid-template-rows)
           5. [grid-template-columns](#grid-template-columns)
           6. [grid-auto-flow](#grid-auto-flow)
           7. [grid-auto-rows](#grid-auto-rows)
           8. [grid-auto-columns](#grid-auto-columns)
           9. [grid-area](#grid-area)
           10. [grid-row](#grid-row)
           11. [grid-column](#grid-column)
           12. [grid-row-start](#grid-row-start)
           13. [grid-row-end](#grid-row-end)
           14. [grid-column-start](#grid-column-start)
           15. [grid-column-end](#grid-column-end)
       36. [ギャッププロパティ](#ギャッププロパティ)
           1. [grap](#grap)
           2. [column-gap](#column-gap)
           3. [row-gap](#row-gap)
       37. [box配置系プロパティ](#box配置系プロパティ)
           1. [justify-self](#justify-self)
           2. [justify-items](#justify-items)
           3. [justify-content](#justify-content)
           4. [align-self](#align-self)
           5. [align-items](#align-items)
           6. [align-content](#align-content)
           7. [place-self](#place-self)
           8. [place-items](#place-items)
           9. [place-content](#place-content)
       38. [コンテナクエリ系プロパティ](#コンテナクエリ系プロパティ)
           1. [container](#container)
           2. [container-name](#container-name)
           3. [container-type](#container-type)
       39. [スクロール関連](#スクロール関連)
           1. [scroll-hehavior](#scroll-hehavior)
           2. [scroll-snap-type](#scroll-snap-type)
           3. [scroll-snap-align](#scroll-snap-align)
           4. [scroll-snap-stop](#scroll-snap-stop)
           5. [scroll-margin(-top/-right/-bottom/-left)](#scroll-margin-top-right-bottom-left)
           6. [scroll-padding(-top/-right/-bottom/-left)](#scroll-padding-top-right-bottom-left)
           7. [scroll-behavior(-top/-right/-bottom/-left)](#scroll-behavior-top-right-bottom-left)
           8. [scrollbar-gutter](#scrollbar-gutter)
           9. [overflow-anchor](#overflow-anchor)
       40. [ユーザーインターフェース系プロパティ](#ユーザーインターフェース系プロパティ)
           1. [cursor](#cursor)
           2. [caret-color](#caret-color)
           3. [pointer-events](#pointer-events)
       41. [ブロック・インライン系プロパティ](#ブロックインライン系プロパティ)
           1. [block-size](#block-size)
           2. [inline-size](#inline-size)
           3. [max-(min-) block-(inline-) size](#max-min--block-inline--size)
           4. [border-block(-inline)](#border-block-inline)
           5. [border-block-start(-end)](#border-block-start-end)
           6. [border-inline-start(-end)](#border-inline-start-end)
           7. [border-block(-inline)-color](#border-block-inline-color)
           8. [border-block(-inline)-start(-end)-color](#border-block-inline-start-end-color)
           9. [border-block(-inline)-start(-end)-style](#border-block-inline-start-end-style)
           10. [border-block(-inline)-width](#border-block-inline-width)
           11. [border-block(-inline)-start(-end)-width](#border-block-inline-start-end-width)
           12. [inset-block(-inline)](#inset-block-inline)
           13. [inset-block(-inline)-start(-end)](#inset-block-inline-start-end)
           14. [margin-block(-inline)](#margin-block-inline)
           15. [margin-block(-inline)-start(-end)](#margin-block-inline-start-end)
           16. [padding-block(-inline)](#padding-block-inline)
           17. [padding-block(-inline)-start(-end)](#padding-block-inline-start-end)
           18. [overflow-block(-inline)](#overflow-block-inline)
           19. [overscroll-behavior-block(-inline)](#overscroll-behavior-block-inline)
           20. [scroll-margin-block(-inline)](#scroll-margin-block-inline)
           21. [scroll-margin-block(-inline)-start(-end)](#scroll-margin-block-inline-start-end)
           22. [scroll-padding-block(-inline)](#scroll-padding-block-inline)
           23. [scroll-padding-block(-inline)-start(-end)](#scroll-padding-block-inline-start-end)
           24. [border-start(-end)-star(-end)-radius](#border-start-end-star-end-radius)
           25. [contain-intrisnic-block(-inline)-size](#contain-intrisnic-block-inline-size)




# CSS入門の自分用まとめ（参考：とほほのCSS入門、というか写し）
参照日：2025/6/16 (Thu)


## 基本セレクタ

### tagname{...}

型セレクタと呼ばれる。適用する要素をタグ名で指定する。


```css
h1 {color:red;}
```

### .class{...}

クラスセレクタと呼ばれる。ドット（.）で始まる名前はクラス名を示す。
一つの要素に複数のクラス名を指定することもできる。

```css
.pretty{color:lime;}
```

.classはほかのセレクタに加えて記述することもできる。

```css
h1.pretty{...} /*<h1 class="pretty">の要素にマッチする*/
.pretty.cool{...}/*<p class="pretty cool></p>の要素にマッチ*/
```

### #id{...}

IDセレクタと呼ばれる。ハッシュ（＃）で始まる名前はIDを示す。同じクラス名を持つ要素は複数あってもよいが、同じIDを持つ要素は一つにしなければならない。
```css
#header {color:blue;} /*<... id="header></...>のような要素にマッチする*/
```

#idもほかのセレクタと組み合わせれる。
```css
div#header {...} /*<div id="header"></div>のような要素にマッチ*/
```

### *{...}

全称セレクタと呼ばれる。アスタリスク（*）はすべての要素にマッチする。

```css
* {color:red;}
```

### namespace | E

ネームスペースセパレータと呼ばれる。nsには@namespace（後述）で指定したネームスペースを指定する。

```css
*|p {color:red;} /*全てのネームスペースのp要素とマッチする*/
```

## 属性セレクタ

### [attr]

attr(hoge)属性を持つ要素にスタイルを適用する。

```css
p[class] {color:red;} /*属性にclassが付加されているものに適用する*/
```

### [attr=value]

attr属性がvalである要素にスタイルを適用する。

```css
h1[class="example"]{color:red;}/*class="example"の属性を持つh1要素にスタイルを適用する。*/
h1[id="xyz"]{...}/*id="xyz"にマッチする。*/
```

### [attr~=value]

attr属性にvalを一つでも含むものにスタイルを適用する。

```css
h1[class~="cool"] {color:red;} /*class="cool ...."のような要素に適用する。*/
```

### [attr|=value]

prefixとしてattr="val"やハイフンを加えたattr="val-"にマッチする属性を持つ要素にマッチする。

```css
[hrefland|="en"] {color:red;}/*
hreflang="en"やhreflang="en-US"の属性を持つ要素にマッチする*/
```

### [attr^=value]

attr属性がvalで始まる要素にマッチする

```css
[href^="http://"]{color:red;} /*attr属性の値がvalで始まる要素にマッチする*/
```

### [attr$=value]

attr属性の値がvalで終わる要素にマッチする

```css
[href$=".html"] {color:red;}/*href属性の値が.htmlで終わる要素にマッチする*/
```

### [attr*=value]

attr属性の値がvalを含む要素にマッチする。
~=との違いは一つ丸々含むか、一部だけでも良いかの違い。

```css
[href*="www.tohoho-web.com"] {color:red;}
```

### [ns|attr]

@namespaceで指定した名前空間ns中のattr属性を持つ要素にスタイルを適用する。

```css
[svg|title] {color:red;}
```

## 結合子

### E,F,...{...}

セレクタリストと呼ばれる。E要素およびF要素にマッチする。

```css
h1,h2,h3,h4,h5,h6 {color:red;}
/*h1,h2,h3,h4,h5,h6に対してマッチする。*/
```

```css
h1,.cool,#zy123,:visited,[src^="http://"]{color:red;} 
/*h1要素、coolクラスの要素、idがzy123の要素、訪問済みリンク、src属性が"http://"で始まる要素に対してスタイルを適用する。*/
```

### E F ...{...}

子孫結合子と呼ばれる。E要素の子孫として出現するF要素にマッチする。

```css
ul li{color:red;}/*ul要素の子孫として適用するli要素に対してスタイルを適用する。*/
```

```css
ul li {color:red;}
ul ul li {color:blue;}
ul ul ul li {color:green;}
```

### E > F
子結合子と呼ばれる。E要素の子として出現するF要素にマッチする。直の子要素である要素に対してのみスタイルが適用される。

```css
body > div {margin:10px}
```

### E+F
次兄弟結合子と呼ばれる。E要素の直後に兄弟要素として出現するF要素にマッチする。

```css
h1 + div {border:1px solid gray;}
```
```html
<div>適用なし</div>
<h1>ヘッダ</h1>
<div>適用あり</div>
<div>適用なし</div>
```

### E ~ F {...}

後続兄弟結合子と呼ばれる。E要素の後に兄弟要素として出現するF要素にマッチする。

```css
h1 ~ div {color:red;}
```

```html
<div>適用なし</div>
<h1>ヘッダ</h1>
<div>適用あり</div>
<div>適用あり</div>
```

## 疑似クラス

### 入力疑似クラス


#### :autofill

ブラウザが自動補完した<"input">要素にマッチする

#### :enabled

要素がenableの状態の時にマッチする。

#### :disabled

要素がdisableの状態の時にマッチする。

#### :read-only

読み取り専用'readonly'が指定されている要素と一致する。

#### :read-write

ユーザーが編集可能な要素と一致する。

#### :placeholder-shown

プレースホルダーが表示されている'input','textarea'要素にマッチする。検索すると様々なCSSテクニックでりようされているのがよくわかる。

```css
input:placeholder-shown {background-color:skyblue;}
input:not(:placeholder-shown) {backgorund-color:pink;}
```

#### :default

デフォルトのinput要素にマッチする。

#### :indeterminate
ラジオボタンやチェックボックスで要素のチェック状態が不定の時にマッチする。

```css
:indeterminate {background-color:#ff999;}
```

#### :blank

何も入力されていない入力部品にマッチする。

```css
input:blank {...}
```

#### :valid

バリデーションが成功したフォーム要素と一致する。

```css
input:valid {background-color:skyblue;}
```

#### :invalid

バリデーションが失敗したフォーム要素と一致する。

```css
input:invalid {background-color:pink;}
```

#### :in-range

input要素のmin,max属性で指定した範囲で範囲内の場合にマッチする。

```css
input:in-range {background-color:skyblue;}
```

#### :out-of-range
input要素のmin,max属性で指定した範囲の範囲外の場合にマッチする。

```css
input:out-of-range {background-color:pink;}
```

#### :required

required属性が指定された入力部品にマッチする。

```css
input:required {background-color:pink;}
```

#### :optional

required属性が指定されていない、入力が必須でない入力部品要素にマッチする。
```css
input:optional {background-color:silver;}
```


### 言語疑似クラス

#### :lang(c)

言語情報がcである要素にマッチする。

```css
:lang(ja) {color:red;}
:lang(en) {color:blue;}
```

### 位置疑似クラス

#### :link

未訪問のリンク要素にマッチする。

```css
:link {color:red;}
a:link {color:red;}
```

#### :visited

訪問済みのリンク要素にマッチする。

```css
:visited {color:red;}
a:visted {color:red;}
```

#### :target

URLの#idに対応する要素にマッチする。
#section1でアクセスしたときはid="section1"の要素に。#section2でアクセスしたときはid="section2"の要素にマッチする。（飛んだ対象の要素にマッチする）

```css
h1:target{color:red;}
```
### リソース状態疑似クラス

なし

### ツリー構造疑似クラス

#### :root

文章のルート要素にマッチする。html文書ならばhtml要素に。
全体に共通するスタイルを変更させることができる。

```css
:root {color:red;}
```

#### :empty

その要素が、子要素やテキストを持ってない場合にマッチする。

```css
td:empty {background-color:silver;}
```

#### :nth-child(n)

その要素が、親要素から見て、n番目の子要素である場合にマッチする。
nをan+bやan-b、evenやoddの形式も指定できたりする。

```css
tr:nth-child(3) {color:red;} /*3行目のtr要素にマッチする。*/
tr:nth-child(2n) {color:red;}
tr:nth-child(n) {color:red;}
tr:nth-child(even) {color:red;}
```

#### : nth-last-child(n)

その要素が、親要素から見て、後ろからn番目の子要素である場合にマッチする。

```css
tr:nth-last-child(2) {color:red;}
```

#### :first-child

その要素が、親要素から見て、最初の子要素である場合にマッチする。

```css
tr:first-child {color:red;}
```

#### :last-child

その要素が、親要素から見て、最後の子要素である場合にマッチする。

```css
tr:last-child {color:red;}
```

#### :only-child

その要素が、親要素から見て、唯一の子要素である場合にマッチする。

```css
td:only-child {color:red;}
```

#### :nth-of-type(n)

その要素が、親要素から見て、n番目の該当要素である場合にマッチする。

```css
td:nth-of-type(3) {color:red;} /*td要素のみをカウントする*/
```

#### :nth-last-of-type(n)

その要素が、親要素から見て、後ろからn番目の該当要素である場合にマッチする。

```css
td:nth-last-of-type(3) {color:red;}
```

#### :first-of-type

その要素が、親要素から見て、最初の該当要素である場合にマッチする。

```css
td:first-of-type {color:red;}
```

#### :last-of-type

その要素が、親要素から見て、最後の該当要素である場合にマッチする。

```css
td:last-of-type {color:red;}
```

#### :only-of-type

その要素が、親要素から見て、唯一の該当要素である場合にマッチする。

```css
td:only-of-type {color:red;}
```

### ユーザー操作疑似クラス

#### :hover

マウスを載せているなどのポインティングデバイスで示されている要素にマッチする。

```css
:hover {color:red;}
```

#### :active

マウスでクリック中など、アクティブな要素にマッチする。

```css
:active {color:red;}
```

#### :focus

フォーカスが当てられている要素にマッチする。

```css
:focus {color:red;}
```

#### :focus-visible

フォーカスが当てられていて、かつ、ブラウザが強調表示を行うべきと判断した要素にマッチする。

```css
:focus-visible {outline:2px solid #66f;border-radius: .2rem;}
```

### 論理結合疑似クラス

#### :is(...) , where(...)

```css
h1.sub, h2.sub, h3,sub{...}
:is(h1,h2,h3).sub {...} /*まとめられる*/
```

#### :not(...)

:not()は否定を表す。

```css
:not(h1)
button:not([disabled]) {...} /*disabled以外のボタン要素*/
```

### 表示状態疑似クラス

#### :open

開いている状態の'dialog','details'および選択表示中の'select','input'にマッチする。

```css
dialog:open {...}
```

#### :fullscreen

JavascriptのrequestFullscreen()などによって全画面モードで表示されている要素にマッチする。

```css
:fullscreen {...}
```

#### :modal

JavascriptのshowModal()などによってモーダルモードで表示されている要素にマッチする。

```css
dialog:modal {...}
```

#### :picture-in-picture
JavascriptのrequestPictureInPicutre()などによってピクチャインピクチャモードで表示されている要素(video等)にマッチする。

```css
:picture-in-picture {...}
```

### その他疑似クラス

#### :defined

```css
my-element:not(:defined) {display:none;}
my-element:defined {display:block;}
```

## 擬似要素

### タイポグラフィック擬似要素

#### ::first-line

要素の中の一行目に対してスタイルを適用する。

```css
p::first-line {text-transform: uppercase;}
```

#### ::first-letter

要素の中の一文字目に対してスタイルを適用する。

```css
p::first-letter {text-transform:uppercase;}
```

### ハイライト擬似要素

#### ::selection

選択された箇所に対してスタイルを適用する。

```css
::selection {color:red; background-color:#ffcccc;}
```

### ツリー永続系

#### ::before

指定した要素の先頭に対してスタイルを適用する。

```css
h2::before {content:"・";} /*すべてのh2要素の先頭に・を追加する*/
```

#### ::after

指定した要素の直後に対してスタイルを適用する。

```css
h2::after {content:".";}
```

#### ::marker

liやsummary要素の先頭の黒丸などのマーカーに対してスタイルを適用する。

```css
ul li::marker {color:red;}
```

#### ::placeholder

'input type="text" placeholder="xxx">などのプレースホルダーに対してスタイルを適用する。

```css
input::placeholder {color:#ccc;}
```

#### ::backdrop

トップレイヤーに表示されるダイアログやポップオーバーの背景となる要素に対してスタイルを適用する。

```css
::backdrop {background:rgb(0 0 0 / 20%);}
```

## ルール

### 基本ルール

#### @charset

外部スタイルシートファイルの文字セットを指定する。ファイルの先頭行に記述される。
utf-8 , Shift_JIS , euc-jpなどが指定できる。

```css
@charset "utf-8";
p {color:red;}
```

#### @import

スタイルシートファイルから、他のスタイルシートファイルを読み込む。@importは@charsetを除く他のルールよりも前に使用する必要がある。

```css
@import url(http://www.yyy.zzz/style.css);
@import "http://www.yyy.zzz/style.css";
@import "style_for_print.css" screen and (min-width: 768px) /*メディアタイプ・メディア特性を指定することができる。*/
```

### フォントルール

#### @font-face

カスタムフォントを読み込むことができる。

```css
@font-face{
    font-family:'my-font';
    src:url(../fonts/myfont.woff) format("woff");
    /*他にもfont-style,font-weight,font-stretch...などが指定できる。*/
}
*{
    font-family:'my-font';
}
```

### レイアウト・メディアルール

#### @media

スタイルシートを適用する条件を指定できる。
例えば、スマートフォンとPCで適用するスタイルシートを変更できる。

```css
@media screen{
    em {color:red;}
}
@media print{
    em {font-weight:bold;}
}
```

@mediaに続けて、次のような条件を記述できる。

```css
@media (max-width:767px;) { ... }
@media (min-width:768px) and (max-width:1200px;) { ... }
@media not (monochrome) { ... }
@media screen and (color) , print and (monochrome) { ... } /*カンマはorを表す*/
@media (720px <= width <= 1200px) { ... }
```

条件には下記などの属性を指定することができる。(min-/max-)とあるものはプレフィックスをつけられる。

```css
@media (max-width:767px) { ... }
@media (max-device-height:767px) { ... }
@media (orientation : portrait) { ... }
@media (min-aspect-ratio: 2/1) { ... }
@media (color) { ... }
@media (min-color : 8) { ... } /*などなど*/
```

#### @keyframes

animationプロパティによるアニメーションのフレームを定義する。nameにanimation-nameプロパティで指定するフレーム名を定義する。

```css
@keyframes myframe{
    from {
        color:red;
    }
    to {
        color:blue;
    }
}
.test {
    animation:myframe 2s infinite both;
}
```

## 宣言

### !important

スタイルが適用される優先順位を最優先にする際に用いられる。

```css
div.classb {color:blue;}
div {color:red !important;}
```

## 値

### 'number'

数値を指定する。少数や負数も指定できる。

### 'integer'

整数値を指定する。負数も指定できる。

### 'length'

数値＋単位の形式で長さを指定する。
em,ex,ch,rem,vw,vh,vmin,vmax,cm,mm,Q,in,pt,pc,px

### 'percemtage'

長さや度数をパーセンテージで示す。

### 'string'

文字列を指定する。ダブルクオーテーションやシングルクオーテーションで囲む。

### 'angle'

角度を指定する。
deg,grad,rad,turn
```css
<div style="transform:rotate(15deg); width:60px;">こんにちは</div>
```

### 'color'

色を指定する。
```css
h1 {color:rgb(255,0,0);}
h2 {color:rgba(255,0,0,0.5);}
```

### 'image'
background-imageなどのプロパティでイメージを指定する。

```css
background-image:url(image/back.png);
background-image:linear-gradient(to right,yello,red);
```

### 'position'
background-positionなどで背景画像の位置を指定する際に用いられる。

```css
.top {background-position:top;}
```

### 'frequency'

周波数を表す単位として定義されている。

```css
*{voice-pitch:250Hz;}
```

### 'time'

時間を表す単位として定義されている。

```css
.slidein{
    animation-duration:2.5s;
    animation-name:slidein;
}
@keyframe slidein{
    from{
        margin-left:300px;
    }
    to{
        margin-left:0;
    }
}
```

### 'url'

外部ファイルのURLを指定する。

```css
.d1{
    background-image:url(../image/back.gif);
}
```

### 'cursom-ident'

cssで作成者が定義する識別名。
半角英数字、ハイフン、アンダースコア、エスケープシーケンス、Unicode文字が使える。

### 'initial , revert , inherit , unsert'

```css
.parent{font-size:14px;}
.initial{font-size:initial;} /*仕様で決められた通常要素の値*/
.revert{font-size:revert;}/*ブラウザがh1に対して定めている値*/
.inherit{font-size:inherit;}/*親要素に設定している値。*/
.unset{font-size:unset;}/*継承する場合はinheritと、しない場合はinitialと同じ値。*/
```

## 参照関数

### var()

独自定義した変数を参照する。

```css
:root{
    --default-color:red;
}
.box{
    color:var(--default-color,blue);
    /*--default-colorが指定されていないときはblueを、定義されているなら--default-colorを適応する。*/
}
```

### url()

外部ファイルのURLを指定する。

```css
body {background-image: url(../image/back.gif);}
body {background-image: url(http://www.example.com/image/back.gif);}
```


## 計算関数

### calc()

calc()を用いて、加算、減算、乗算、除算の四則演算を行うことができる。

```css
.col3{
    width:calc(100%*3/12-10px);
}
```

## 比較関数

### min()

min(value1,value2,...)となっているときvalue1,value2,...の最小値を返す。

```css
.box {
    width:min(100%,40rem);
}
```

### max()

最大値を返す。

```css
.box {
    width:max(100%,40rem);
}
```

### clamp()

clamp(min,value,max)のときvalue -> [min,max]を返す。

```css
.box{
    width:clamp(5rem,50rem,10rem);
}
```

## 段階値関数

## 数学関数

## 描画関数

### image-set()

画像形式や解像度の異なる画像の中からブラウザに適した画像を表示する。

```css
.box{
    background-image :url(./image/sample_1x.jpg);
    background-image: -webkit-image-set(
        url(./image/sample_1x.jpg) 1x,
        url(./image/sample_2x.jpg) 2x
    );
    background-image: image-set(
        url(./image/sample_1x.jpg) 1x,
        url(./image/sample_2x.jpx) 2x
    );
    background-image: -webkit-image-set(
        url(./image/sample.avif) type("image/avid"),
        url(./image/sample.jpg) type("image/jpeg")
    );
}
```

## プロパティ

### 全プロパティ

#### all

unicode-bidiとdirectionを除くすべてのプロパティの値をまとめて設定する。
値には'initial,revert,inherit,unset'を指定することができる。

```css
h1{
  all:initial;
  border: 1px solid #999;
}
```

### 色系プロパティ

#### color

テキストの色を指定する。

```css
*{
    color:red;
}
```

#### accent-color

チェックボックス、ラジオボタン、レンジ、プログレスバーなどの色を指定する。

```css
*{
    accent-color:red;
}
```

#### color-scheme

スマートフォンなどのダークモードに対応する。

```css
:root{
    color-scheme:light dark; /*これを設定するとスマホのモードに応じてこれも変わる。*/
}
@media (prefers-color-scheme: dark){
    /*webページにも対応させることができる。*/
    body{
        background-color:#000;
        color:#fff;
    }
}
```

#### opacity

透明度を0.0 ~ 1.0の数値で指定する。

```css
.opacity-30{
    opacity: 0.3;
}
```

#### rgb/rgba

R,G,Bの色をそれぞれ0 ~ 255の10進数、もしくは0~100%のパーセンテージで表す。

```css
*{
    color:rgb(255,0,0);
    color:rgba(255,0,0,0.9);
}
```


#### forced-color-adjust

強制カラーモードへの対応を指定する。

autoの場合、従い、noneの場合無視する。
preserve-parent-colorの場合は、noneと似ているが、親要素が影響を受けている場合、受けた親要素のcolorプロパティを継承する。

```css
*{
    forced-color-adjust:none;
}
```

### グラデーション系プロパティ

#### linear-gradient()

線形グラデーションを指定する。

第一引数はグラデーションの方向を角度またはto方向で指定し、省略した場合はto bottomとみなされる。

第二引数以降には2個以上の色を指定できる。また色の後に長さやパーセンテージを記述すると、開始から終了方向にその長さまたはパーセント分進んだ箇所でその色が始まる。

```css
*{
    background:linear-gradient(to right,yellow, red);
}
```

#### radial-gradient()

放射線状にグラデーションをかける。

```css
*{
    background:radial-gradient(yellow,red,green,blue);
}
```

#### conic-gradient()

円錐形のグラデーションをかける。

```css
*{
    background:conic-gradient(yellow,red,green,blue);
}
```

#### repeating-linear-gradient()

繰り返し線形グラデーションを指定する。引数はlinear-gradient()と同じで、指定した色が領域いっぱいまで繰り返される。

```css
*{
    background:repeating-linear-gradient(to right,yellow 0%,red 10%,green 20%);
}
```

#### repeating-radial-gradient()

繰り返し放射線状グラデーションを指定する。引数はradial-gradient()と同じで、指定した色が領域いっぱいまで繰り返される。

```css
*{
    background:repeating-radial-gradient(yellow 0%,red 10%,green 20%,blue 30%);
}
```

#### repeating-conic-gradient()

繰り返し円錐形グラデーションを指定する。引数はconic-gradientと同じで、指定した色が領域いっぱいまで繰り返される。

```css
*{
    background:repeating-conic-gradient(yellow 0%,red 50%);
}
```

### フォント系プロパティ

#### font

フォントのスタイル、変換、太さ、サイズ、表示高さ、ファミリをまとめて指定する。

```css
*{
    font:100% Arial;
}
```

#### font-style

フォントスタイルを指定する。normal/italic

```css
*{
    font-style:normal;
}
```

#### font-weight

フォントの太さを指定する。

```css
*{
    font-weight:bold; /*normal,bold,bolder,lighter,100~900*/
}
```

#### font-size

フォントサイズを指定する。

```css
*{
    font-size:xx-small;/*xx-small,x-small,small,medium,large...*/
}
```

#### font-family

フォントファミリーを指定する。

```css
*{
    font-family:serif;/*serif,sans-serif,system-ui...*/
}
```

#### font-stretch

フォントの横幅を指定する。

```css
*{
    font-stretch:ultra-condensed;
    /*condensed,semi-condensed,normal,semi-expanded...*/
}
```

#### font-synthesis

ブラウザが太さや斜体等のスタイル、スモールキャプス文字、上付/下付文字をサポートしていない場合に、ブラウザがこれらのフォントを自動生成するかどうかを指定する。

```css
*{
    font-synthesis:none; /*生成しない*/
}
```

#### font-synthesis-style

使用するフォントが、font-weightで指定する太さの太字をサポートしていない場合、利用可能なフォントから自動生成して表示する。

#### font-synthesis-weight

font-styleで指定する斜体をサポートしていないときに自動生成する。

#### font-synthesis-small-caps

font-variant-capsで指定するスモールキャプス文字をサポートしていない場合に自動生成する。

#### font-kerning

となりあう文字の組み合わせによって文字詰めするかどうかを指定する。

```css
*{
    font-kerning:none;
}
```

#### font-variant-numeric

数学に関する表示を制御する。

```css
*{
    font-variant-numeric:normal;
}
```

#### font-variant-caps

小文字・大文字などの表示を制御する。

```css
*{
    font-variant-caps:normal;
}
```

#### font-variant-ligatures

隣り合った文字の合字を制御する。

```css
*{
    font-variant-ligatures:common-ligatures;
}

#### font-variant-position

文字の上付/下付文字を制御する。

```css
.sup{
    font-variant-position:sub;/*上付き文字で表示する*/
}
.super{
    font-variant-position:super;/*下付き文字で表示する*/
}
```

#### font-variant-east-asian

文字を、JIS78,JIS83など、どの書体で表示するかを指定する。

```css
*{
    font-variant-east-asian:normal;
}
```

#### font-optical-sizing

フォントの光学的サイジングをお行うか否かを指定する。フォントを読みやすくするために小さな文字は幅を少し広げたり、大きなフォントは幅を少し定めたりと見栄えの自動調整を行う。

```css
*{
    font-optical-sizing:auto;
}
```

### テキスト系プロパティ

テキスト
#### text-indent

段落の最初の1行などをインデントする。

```css
p {
    text-indent:1em;
}
```

#### text-align

テキストの配置を指定する。

```css
*{
    text-align:center; /*中央寄せ*/
    /*startは開始側寄せ、endは終了側寄せ*/
    /*leftは左、rightは右側寄せ*/
}
```

#### vertical-align

インライン要素やテーブルセルの垂直方向の揃え方を指定する。

```css
*{
    vertical-align:top;
}
```

#### text-transform

テキストを変更する。

```css
*{
    text-transform:capitalize;/*各単語の先頭文字をすべて大文字にする。*/
}
```

#### line-height

行の高さを指定する。

```css
p{
    line-height:auto;
}
```

#### word-spacing

単語間の隙間を指定する。

```css
*{
    word-spacing:normal;
}
```

#### letter-spacing

文字間の隙間を指定する。

```css
*{
    letter-spacing:10px;
}
```

#### user-select

ユーザーがテキストを選択できるかどうかを指定する。

```css
*{
    user-select:text;
}
```

### 改行系プロパティ

#### white-space

要素の中のテキストを、自動改行するか、複数の空白を一つの空白に置換するか、改行を空白に置換するかを指定する。

```css
*{
    white-space:pre-wrap;
}
```

#### word-break

単語間、文字間で表示幅に合わせた自動改行を行うか否かを指定する。

```css
*{
    word-break:normal;
    margin:1em;
    width:200px;
    border:1px solid #666666;
}
```

#### overflow-wrap

単語の途中などで表示領域の横幅による自動改行を許可するか否かを指定する。

```css
*{
    overflow-wrap:normal;
    width: 12.5rem;
    margin: 1em;
    padding: .2rem;
    border: 1px solid #666666;
    font-size: 10pt;
}
```

#### hyphens

長い単語に対するハイフネーションのふるまいを指定する。ハイフネーションが行われると、横幅を超えるような長い単語の途中で改行が行われ、改行前の末尾にハイフン文字が挿入される。

```css
.box1{ hyphens:none; }
.box2{ hyphens:manual; }
.box3{ hyphens:auto; }
```

### テキストデコレーション系プロパティ

#### text-shadow

テキストに影をつける。
```css
.shadow{
    text-shadow:1px 1px 0px #ffffff;
    /*横に1px,縦に1px,半径0pxのぼかし、色#ffffffの影*/
}
```

#### text-decoration(-style/-color)

テキストの装飾線（上線、下線、打消し線）を描画する。-style,-colorの値をまとめて指定する。

```css
.underline{
    text-decoration:underline wavy red;
}
```

#### text-decoration-skip-ink

テキストの装飾線が対象テキストと重なる場合のステップ方法を指定する。

```css
*{
    text-decoration-skip-ink:none;
}
```

#### text-decoration-thickness

テキストの装飾線の太さを指定する。

```css
*{
    text-decoration-thickness:5px;
}
```

#### text-emphasis(-style/-color)

テキストの上部に注意すべき箇所であるということを示す圏点を描画する。-style,-colorの値をまとめて指摘する。

```css
*{
    text-emphasis:filled circle red;
}

#### text-emphasis-position

圏点の位置を指定する。

```css
*{
    text-emphasis-position:over;
}
```

### 文章方向系プロパティ

#### writing-mode

縦書きを指定する。

```css
.box{
    writing-mode:horizontal-tb; /*横書き,左->右*/
    writing-mode:vertical-rl; /*縦書き,右->左*/
    writing-mode:vertical-lr; /*縦書き,左->右*/
}
```

#### text-orientation

writing-modeでvertical-rl/-lrを指定したときの、横書き文字の表示方向を指定する。

```css
.box{
    writing-mode:vertical-rl;
    text-orientation:mixed;/*英語のみ90°回転させる。*/
    text-orientation:sideways; /*ともに90°回転させる*/
}
```

### ルビ系プロパティ

#### ruby-position

ruby要素で記述するルビについて、ルビテキストを配置する場所を指定する。

```css
.box{
    ruby-position:over;
}
```

### 改ページ・改カラム系プロパティ

#### break-before/-after/-inside

印刷時の改ページに加え、columnsによるマルチカラムにおける改カラムを制御する。

```css
.box{
    break-before:auto;
}
```

#### box-decoration-break

インライン要素が改行されたり、ブロック要素が檀久美、改頁する際の、border,border-radius,paddingなどの表示方法を指定する。

```css
.clone{
    box-decoration-break:clone;
}
```

### リスト系プロパティ

#### list-style(-type,-position,-image)

liの黒ぽちのスタイルを指定する。

### カウンター系プロパティ

#### counter-set

#### counter-set　

最初の値を指定する。

#### counter-reset

値をリセットする。

#### counter-increment

その要素のたびに値をインクリメントする。

#### counter()/counters()

カウンターを挿入する。counters()の場合は入れ子構造のものも挿入することができる。

```css
body {
    counter-set: my-chapter 5;
}
h1 {
    font-size:24px;
    counter-increment: my-chapter;
}
h1::before{
    content: counter(my-chapter) ". ";
}
```

```css
ol {
    counter-reset: cnt;
    list-style: none;
    padding-left: .5rem;
}
li::before{
    content: counters(cnt,".") ") ";
    counter-increment: cnt;
}
```

### テーブル系プロパティ

#### caption-side

テーブルのキャプションをテーブルの上部に表示するか、下部に表示するかを指定する。

```css
.sample{
    caption-side: top;
}
```

#### table-layout

テーブルのレイアウト方式を指定する。

```css
.table{
    table-layout: fixed;
}
```

#### border-collapse(-spacing)

隣り合ったテーブルの枠線の描画方法を指定する。

```css
.sample-collapse{
    border-collapse: collapse; /*重なり合わせて表示する。*/
    border: 1px solid #888;
    margin: 0em 1em 1em 1em;
}
.sample-separate{
    border-collapse: separate; /*離す。隙間の間隔はborder-spacingで指定する。*/
    border-spacing: 2em;
}
```

#### empty-cells

テーブルセルの中身が空、または不可視文字のみで構成されている場合にセルを表示するか否かを指定する。

```css
.empty-cells{
    empty-cells: show; /*表示する*/
    empty-cells: hide; /*表示しない*/
}
```

### コンテント作成系プロパティ

#### content

疑似要素::before,::afterとともに用いて、要素の前方または後方に文字、画像、カウンターなどを挿入する。

```css
.content-string::before{
    content: "[string] ";
}
```

### 印刷系プロパティ

#### size

印刷時のサイズを指定する。

```css
@page{
    size:A4 portrait;
}
```

#### orphans/widows

印刷時、ページ下部（上部）の段落に最低限印刷すべき行数を指定する。
(orphans) Page.1下部の段落3が3行しかない場合、その段落3は次のページに印刷される。

```Css
body{
    orphans:4;
    widows:4;
}
```

### ブレンド系プロパティ

#### mix-blend-mode

背景と要素が重なる部分の、色のブレンド方式を指定する。

```css
.elem{
    mix-blend-mode: darken;
}
```

#### background-blend-mode

background-imageによる背景と、さらにその下側にある背景が重なる部分の、色のブレンド方式を指定する。

```css
div{
    width:200px;
    height:200px;
    background-size: 200px 200px;
    background-repeat: no-repeat;
    background-image: linear-gradient(to right, #000000 0%,#ffffff 100%), url('ducky.png');
    background-blend-mode: difference,normal;
}
```

### 配置系プロパティ

#### position

要素のポジショニングの方法を指定する。

| 値 | 説明 |
|----|-----|
|static| 通常の位置に配置される。 |
|relative| 要素が通常配置されるべき場所から、topやleft等で指定されたオフセット分ずらされた場所に配置される。 |
|absolute| 親要素がposition:staticの時はウィンドウの左上、親要素がそれ以外の時は左上を基準位置とし、topやleft等で指定されたオフセットの絶対位置に表示する。 |
|sticky| topと組み合わせて指定した場合、ページを下にスクロールして画面からはみ出しそうになったら、ページ上部に張り付く。 |
|fixed| 通常の位置に表示されるが、ページをスクロールしても移動しない。 |

#### top/right/bottom/left

上端、右端、下端、左端からの距離を指定する。

```css
.box{
    position:absolute;
    bottom:10px;
    right:10px;
}
```

#### inset

top,bottom,right,leftを同時に指定する。

```css
.test{
    position:relative;
    inset: 1rem 2rem;
}
```

#### z-index

要素同士が重なって表示されている場合の、優先順位を指定する。
positionにstatic以外の値が設定されている要素に対して有効。

```css
.sample{
    position:absolute;
    z-index:3;
    top:60px;
    left:40px;
    background:#99ff99;
}
```

### 表示系プロパティ

#### float

画像などの表示位置を指定する。leftやrightを指定すると、テキストがその周りをまわりこむように表示する。

```css
.float_left{
    float:left;
}
```

#### clear

floatで設定したテキストの回り込み設定を解除する。

```css
.clear_none{
    clear:none;
}
```

#### overflow(-x/-y)

コンテンツが要素の高さや横幅を超えた場合に、スクロールして表示する、表示しない、はみ出して表示するなどを指定する。

```css
.mybox{
    border: 1px solid #999999;
    width: 400px;
    height: 100px;
    margin-bottom: 2em;
    overflow: scroll;
}
```

#### overflow-clip-margin

overflow-clipが適応された要素に対して、どこまで内部コンテンツがはみ出してよいかを指定する。

#### text-overflow

overflow:hiddenで領域からあふれた文字を日表示する際に、非表示にしたことを示す文字列を指定する。

```css
.box{
    width: 15rem;
    border: 1px solid #ccc;
    margin-bottom: .5rem;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}
```

#### visibility

要素を表示する・しないを切り替える。

```css
p {
    visibility:hidden;
}
```
#### display

要素をどのような形式で表示するかを指定する。

```css
.memo{display: none;}
```

| 値 | 説明 |
| -- | --- |
| block | 要素が縦に並び、幅と高さが指定でき、marginとpaddingを使って余白を自由に調整できる。|
| inline | 要素が横に並ぶが、幅と高さが指定できず、上下の余白がmarginで調整できない。|
| inline-block | 要素が横に並び、幅と高さが指定でき、marginとpaddingを使って余白が指定できる。|
| flex/inline-flex | 要素を建てに分割するなどのフレックスコンテナとして表示する。|
| grid | グリッドを表示する。 |
| none | 要素を非表示にする。 |
| contents | ??? |

#### appearance

フォーム部品に対してブラウザのデフォルトのデザインを変更する。

```css
.myex input[type="checkbox"] {
    appearance: none;
    outline: 1px solid #999;
    width: 12px;
    height: 12px;
    line-height: 12px;
    text-align: center;
    vertical-align: top;
    position: relative;
}
.myex input[type="checkbox"]:checked::before {
    content: "✓";
    position: absolute;
    left: 2px;
    top: -1px;
    font-size: 12px;
}

```

#### contain

ページのレンダリング性能を高めたり、コンテンツの中身がほかのコンテンツへの影響することを抑止するための「css封じ込め：を行う

```css
.box{
    contain: none;
}
```
<!--
#### content-visibility

#### contain-intrinsic-height

#### contain-intrinsic-size

#### contain-intrinsic-width

-->

### margin系プロパティ

#### margin(-top/-right/-bottom/-left)

marginは、borderと周りのコンテンツとの間の隙間に相当する。

```css
.box{
    margin:1em;
}
```

#### padding系プロパティ

#### padding(-top/-right/-bottom/-left)

paddingは、borderとその内側のコンテンツとの間に相当する。

```css
.box{
    padding:3px;
}
```

### サイズ系プロパティ

#### width/height

要素の横幅・高さを指定する。

```css
main{
    width:80%;
    height:100px;
}
```

#### min-/max- width/hright

最小（最大）の横幅・高さを指定する。（文章がそれより長い場合はboxが伸びる）


```css
.box{
    min-width:80px;
}
```

#### box-sizing

heightやwidthが対象とする領域を指定する。

#### resize

overflowにvisible以外の値が設定された要素に対して、縦・横方向のリサイズを許可するか否かを指定する。

```css
.box{
    resize:both;
}
```

#### aspect-ratio

矩形の縦横比を指定する。

```css
.box{
    aspect-ratio: auto;
}
```

### 背景系プロパティ

#### background

背景画像についてまとめて指定する。

#### background-color

背景色を指定する。

#### background-image

背景画像を指定する。

#### background-repeat

背景の繰り返し方法を指定する。

#### background-attachment

画面のスクロールバーに追従して、背景画像もスクロールさせるか否かを指定する。

#### background-position(-x/-y)

画面表示する際の基準位置を指定する。

#### background-clip

背景画像を表示する領域を指定する。

#### background-origin

背景画像を表示する際の基準位置を指定する。

#### background-size

背景画像のサイズを指定する。

```css
.box{
    background-color: black;
    background-image: url(./image/back.gif);
    background-repeat: repeat-x;
    background-attachment: scroll;
    background-position: 50% 50%;
    background-clip: border-box;
    background-size:auto;
}
```

### border系プロパティ

#### border(-top/-right/-bottom/-left) -(width/-style/-color)

ボーダーラインの太さ、線種、色をまとめて指定する。

```css
.box{
    border: 1px solid gray;
}
```

#### border(-top-left/-top-right/-bottom-left/-bottom-right)-radius

角の丸いボーダーラインを描画する。

```Css
.box{
    border-radius: 10px;
    border: 6px solid red;
    background-color: #cc9999;
    height: 32px;
    width: 120px;
}
```

#### border-image

画像を用いたボーダーを表示する。

```css
#d1{
    width: 120px;
    height: 60px;
    border-image: url(./image/border-image.png) 10 / 10px round;
    border-style: solid;
}
```

#### border-image-source

ボーダーに用いる画像のurlを指定する。

#### border-image-slice

ボーダーイメージの元画像のスライス方法を指定する。

#### border-image-width

ボーダーの太さを指定する。

#### border-image-outset

ボーダーイメージをボーダーボックスを超えて広げる量を指定する。

#### border-image-repeat

繰り返し方法を指定する。

```css
.box{
    border-image-source: url(./image/border-image.png);
    border-image-slice: 10;
    border-image-width: 10px;
    border-image-repeat: round;
    border-style: solid;
    margin: 10px;
    padding: 10px;
    box-sizing: border-box;
}
```

#### box-shadow

ボーダーラインに影を付ける。

```css
.sample_multiple{
    box-shadow: 5px 5px 10px 0px #333333, 5px 5px 10px 0px #333333 inset;
}
```

### アウトライン系プロパティ

#### outline(-width/-style/-color)

リンクやフォーム部品がフォーカス状態になったときに表示されるうすい枠線の太さ、形式、色を指定する。

#### outline-offset

フォーカスが当てられたときなどに表示するアウトラインと、ボーダー間との距離を指定する。

### イメージ系プロパティ

#### image-reading

画像を拡縮表示する際のアルゴリズムを指定する。

```css
.auto{
    image-rendering: auto;
}
```

#### object-fit

画像やビデオの横幅や高さを指定したときに、オブジェクトをどのように拡縮するかを指定する。

#### object-position

object-fitを指定した場合のオブジェクトの表示位置を指定する。

```css
.img1{
    object-fit: none;
    object-position: center top;
}
```

### マスキング系プロパティ

#### clip-path

矩形、円形、楕円形、星形などの領域を抜き出し、表示する。

```css
.my-example{
    img{
        width: 100px;
        height: 100px;
        clip-path: polygon(50px 0px, 20px 100px, 100px 40px, 0px 40px, 80px 100px);
    }
}
```

#### mask-image

マスクイメージを指定する。カンマ連結で複数指定できる。

```css
.box{mask-image: url(mask.png) , url(mask2.png);}
```

#### mask-size

マスクイメージのサイズを指定する。

```css
.box{mask-size: auto;}
```

#### mask-repeat

マスクイメージの繰り返しスタイルを指定する。

```css
.box{mask-repeat: repeat;}
```

#### mask-position

マスクイメージの位置を指定する。

```css
.box{mask-position: 10px 10px;}
```

#### mask-origin

マスクイメージの開始位置を指定する。

#### mask-clip

描画範囲を指定する。

#### mask

mask-を一括指定する。

### フィルタ系プロパティ

#### filter

画像などの要素に対して、ぼかし、影つけ、透明化などのフィルタを適用する。

#### blur()

要素をぼかす。

```css
.box{
    filter:blur(2px);
}
```

#### brightness()

要素の明暗を調整する。

```css
.box{
    filter:brightness(1.7);
}
```

#### contrast()

要素のコントラストを指定する。

```css
.box{
    filter:contrast(2.0);
}
```

#### drop-shadow()

要素に影を付ける。

```css
.box{
    filter:drop-shadow(5px 5px 2px #999);
}
```

#### grayscale()

要素をグレーにする。

```css
.box{
    filter:grayscale(1.0);
}
```

#### hue-rotate()

要素の色相を変換する。

```css
.box{
    filter:hue-rotate(180deg);
}
```
#### invert()

要素の階調を反転させる。

```css
.box{
    filter:invert(100%);
}
```

#### opacity()

要素を透明にする。

```css
.box{
    filter:opacity(30%);
}
```

#### saturate()

要素の彩度を調整する。

```css
.box{
    filter:saturate(200%);
}
```

#### sepia()

要素をセピア調にする。

```css
.box{
    filter:sepia(0.5);
}
```

### 操作系プロパティ

#### touch-action

スマホやタブレットにおいて、パンやズームなどの操作を抑制する。

```css
.content{
    touch-action: pan-x;
}
```

### トランスフォーム系プロパティ

#### transform

X軸、Y軸、Z軸方向の移動を行う。値を一つ設定するとX、二つ設定するとX,Y、三つ設定するとX,Y,Zで移動する。

#### transform-origin

回転させる場合の中心点を指定する。

#### transform-style

設定した要素の、子要素を三次元変換した結果を二次元的に表示するか、三次元的に表示するかを指定する。

#### transform-box

transformの対象とする領域を指定する。値はbox-sizingと同じ。

#### perspecgive

子要素に対してtransformで三次元変換を行う際の、要素の中心から視点までの距離を指定する。

#### perspective-origin

transformで要素を変換し、perspectiveで視点を移動する場合の視点の原点を指定する。

#### backface-visibility

transformで要素を回転させた際に、背面を表示する・市内を指定する・トランプカードを回転させるように、表のパネルと、180°回転した裏のパネルを重ね合わせて表示する際、表示されるときは表示しないように制御するのに有効。

#### translate() / translateX/Y/Z/3d()

要素をx軸方向にtx,y軸方向にty,z軸方向にtzの長さ分移動させる。

#### scale() / scaleX/Y/Z/3d()

要素をx軸方向にsx,y軸方向にsy,z軸方向にsz倍拡縮する。

#### rotate() / rotateX/Y/Z/3d()

要素をangle分回転させる。

#### skew() / skewX/Y()

要素を横方向にax,縦方向にayだけ傾斜させる。

#### matrix()

translate(),scale(),skew()を同時に指定したような行列変換を行う。sx,ay,ax,sy,tx,tyで指定する。

#### matrix3d()

元要素のx,y,z座標上の位置を、4*4ベクトル演算を用いて変換した場所に表示する。

```css
.test{
    transform: translate(100px,10px) rotate(10deg);
    transform-origin: 50% 50%;
}
```

### トランジション系プロパティ

#### transition
transition-property,duration,timing-function,delayを指定する。

#### transition-property

対象とする属性名を指定する。allを指定するとすべての属性が対象となる。

#### transition-duration

transitionにかける時間を指定する。

#### transition-timing-function

変化の具合を指定する。linearなど

#### transition-delay

開始するまでの遅延時間を指定する。

```css
.test{
    width: 100px; height: 30px;
    background: #f66;
    transition-property: width;
    transition-duration: 0.2s;
    transition-timing-function: linear;
    transition-delay: 0.5s;
}
.test:hover{
    width: 300px;
}
```

### アニメーション系プロパティ

#### animation
アニメーションに関するプロパティを指定する。

#### animation-name

適用するアニメーションのフレーム定義を、@keyframesで定義した名前で指定する。

#### animation-duration

アニメーションにかける時間を指定する。

#### animation-timing-function

アニメーションの変化のタイミングを指定する。

#### animation-delay

アニメーションを開始する時間を指定した時間分遅延させる。

#### animation-iteration-count

アニメーションを繰り返す回数を指定する。infiniteで無限に繰り返す。

#### animation-direction

アニメーションの実施方向を指定する。

#### animation-fill-mode

終了時のスタイルの適用ルールを指定する。

#### animation-play-state

アニメーションを実行、または一時停止の状態にする。

```css
@keyframes myframe{
    from{
        color: #66f;
        font-size:20pt;
    }
    to{
        color: #f66;
        font-size:24pt;
    }
}
.test{
    position:absolute;
    animation-name: myframe;
    animation-duration: 0.5s;
    animation-timing-function: ease-in;
    animation-delay: 0s;
    animation-iteration-count: infinite;
    animation-direction: both;
    animation-play-state: running;
}
```

### シェイプ系プロパティ

#### shape-outside

floatでテキストの回り込みを行う際、矩形だけではなく円形や三角形など様々な形に添ってテキストを回り込ませることができる。

#### shape-margin

テキストの回り込みを指定する際のmarginを指定する。

#### shape-image-threshold

テキストの回り込みを行う際、テキストの表示位置を決めるための透明度を指定する。

```css
#img1{
    height: 200px; width: 200px;
    float: left;
    background-image: linear-gradient(140deg,black,transparent 50%, transparent);
    shape-outside: linear-gradient(140deg,black,transparent 50%, transparent);
    shape-margin: 2rem;
    shape-image-threshold 0.2;
}
```

### モーションパス系プロパティ

#### offset-path

モーションパスのパスを指定する。ray(...)やurl(...),circle()やpath()などで指定できる。

#### offset-distance

パス上の距離または長さをパーセンテージで指定する。

#### offset-position

開始位置が明確に指定されないときの開始位置を指定する。

#### offset-rotate

移動体の回転方向を指定する。

```css
.ray_box{
    position: absolute;
    width: 10px; height: 10px;
    background: red; border-radius:50%;
    offset-path: path("M50,0 A50,50 0 1,1 -50,0 A50,50 0 1,1 50,0");
    offset-rotate:auto;
    animation: move 4s linear infinite;
    transform: translate(150px,150px);
}
```

### マルチカラム系プロパティ

#### columns(-count/-width)

マルチカラムの幅、カラム数をまとめて指定する

#### column-rule(-color/-style/-width)

カラム間の罫線の幅、スタイル、色をまとめて指定する。

#### column-span

マルチカラムの中に章題を記載するときなど、その要素がすべてのカラムを跨いで表示させるか否かを指定する。

#### column-fill

マルチカラムの各カラムの行数に関するアルゴリズムを指定する。

```css
.muoticol_box{
    columns: 3;
    column-rule: 1px dashed red;
}
```

### フレックスボックス

#### flex

flex-grow,flex-shrink,flex-basisをまとめて指定する。

シンプルに横並びにしたい場合や、要素が増える可能性がある場合、また両端揃えにしたい場合に使われる。

#### flex-grow(-shrink)

フレックスアイテムの伸長係数・圧縮係数を指定する。フレックスアイテムの横幅の合計が、フレックスコンテナのコンテンツ領域の幅に達しない場合に、伸長係数に従ってフレックスアイテムの横幅が伸長・圧縮される。

#### flex-basis

フレックスアイテムの横幅（高さ）を指定する。

#### flex-flow

flex-directionとflex-wrapをまとめて指定する。

#### flex-direction

フレックスアイテムを並べる方向を指定する。

#### flex-wrap

フレックスアイテムがフレックスコンテナに収まらない場合、はみ出しても一列に並べて表示するか、複数行に改行して表示するかを制御する。

#### order

フレックスアイテムや、フレックスコンテナ内の絶対位置指定に対して、表示する順序を指定する。

```css
.boxa{ flex:1; background-color:#fcc; }
.boxb{ flex:2; background-color:#cfc; }
```

### グリッド

#### grid

各行の高さ、各列の高さをそれぞれ指定する。

グリッドを意識したデザインであったり、要素が不確定に増えないレイアウトであった場合によく使われる。

```css
.container-grid{
    display: grid;
    grid: 2rem 2rem / 4rem 4rem 4rem;
}
```

#### grid-template(-areas/-row/-columns)

-template-rowsとtemplate-columnsをまとめて指定したり、エリア名、ライン名を定義したりする。

```css
.container-grid{
    grid-template:
        "head head head"
        "menu main side"
        "foot foot foot";
}
```

#### grid-auto-flow

グリッドアイテムを並べる方向をrowまたはcolumnで指定する。denseを指定すると、空きスペースをなるべく埋めるように配置する。

```css
.grid-container-row{
    display: grid;
    grid-auto-flow: row;
    grid-template-rows: 2rem 2rem;
    grid-template-columns: 4rem 4rem;
}
```

#### grid-auto-rows(-columns)

グリッドで区切られた領域のデフォルトの高さと横幅を指定する。

```css
.grid-container{
    display: grid;
    grid-auto-rows: 2rem;
    grid-auto-columns: 4rem;
    grid-template-areas: "a a a";
}
```

#### grid-area(-row/-column)(-start/-end)

グリッドのアイテムに対して、どの位置に表示するかを指定する。
gridやgrid-template-areasで定義したエリア名を指定するか、もしくはグリッド戦の開始位置・終了位置を指定する。

```css
.header{
    grid-area: header;
}
.footer{
    grid-row: 1 / 3;
    grid-column: 1 / 2;
}
```

### ギャッププロパティ

#### (row-/column-)gap

マルチカラム、フレックス、グリッド間の列方向、行方向の隙間をまとめて指定する。

```css
.multicol{
    columns: 3;
    gap: 3rem;
}
```

### box配置系プロパティ

#### (justify/align/place)-(self/itmes/content)

justify-は主軸方向のレイアウトを、align-は交差軸方向のレイアウトを制御する。place-は主軸と交差軸をまとめて指定する。

-selfはアイテムに対して直接指定するが、-itmesや-contentはコンテナに指定してその子アイテムのレイアウトを制御する。また、flex-wrap:wrapなどでアイテムが改行されている場合や、グリッドで行・列の概念がある場合、-itmes は 一つの行や列の中での、個々の子アイテムの位置を制御するのに対して、-contentは、行や列自体をどのように配置するかを制御する。

startやend,normalやstretch,centerなどが指定できる。

```css
.item{
    grid-area: 1/2/3/4;
    justify-self: start;
}
```

### コンテナクエリ系プロパティ

#### container

#### container-name

#### container-type

### スクロール関連

#### scroll-hehavior

#### scroll-snap-type

#### scroll-snap-align

#### scroll-snap-stop

#### scroll-margin(-top/-right/-bottom/-left)

#### scroll-padding(-top/-right/-bottom/-left)

#### scroll-behavior(-top/-right/-bottom/-left)

#### scrollbar-gutter

#### overflow-anchor

### ユーザーインターフェース系プロパティ

#### cursor

#### caret-color

#### pointer-events

### ブロック・インライン系プロパティ

#### block-size

#### inline-size

#### max-(min-) block-(inline-) size

#### border-block(-inline)

#### border-block-start(-end)

#### border-inline-start(-end)

#### border-block(-inline)-color

#### border-block(-inline)-start(-end)-color

#### border-block(-inline)-start(-end)-style

#### border-block(-inline)-width

#### border-block(-inline)-start(-end)-width

#### inset-block(-inline)

#### inset-block(-inline)-start(-end)

#### margin-block(-inline)

#### margin-block(-inline)-start(-end)

#### padding-block(-inline)

#### padding-block(-inline)-start(-end)

#### overflow-block(-inline)

#### overscroll-behavior-block(-inline)

#### scroll-margin-block(-inline)

#### scroll-margin-block(-inline)-start(-end)

#### scroll-padding-block(-inline)

#### scroll-padding-block(-inline)-start(-end)

#### border-start(-end)-star(-end)-radius

#### contain-intrisnic-block(-inline)-size
