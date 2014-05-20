# BabaScript: A Programming Framework for Real-world Entertainment.

## Abstract

We introduce the "BabaScript" programming system that is useful for
writing scripts required for real-world entertainment scenarios
where both computers and humans are involved.
BabaScript is a JavaScript-based programming system that can handle
human behavious in the same way as handling the behaviors of computers.
A BabaScript program can ask a person in the real world to do something
and receive the result, just like
a conventional computer program can calculate a formula and
get the result value.
Using BabaScript, various real-world activities of computers and humans
can be described as simple scripts,
and complicated real-world entertainment scenarios can be described
easily.

<!--
Conventional programming languages are designed for describing
the behaviors of computer systems, and not designed for describing
human behavious.

If a programming system can handle both computer resources and
humans in the similar way, various 



Using conventional programming languages,



Many recent programming systems support croudsourcing features
where computer programs can utilize human resources in the whole world,
computer resources and human resources are not fully integrated in
most of the systems.
Using the BabaScript system, all the computer activities and
human activities can be described in a powerful and simple
programming language, and

interactions required for real-world entertainment can be described

all the intelligent entities in the real world connected to the Internet
can be programmed in a consistent way.
-->

In this paper,
we describe the basic design of BabaScript, and
show how BabaScript can be used for
various real-world entertainment involving computers and humans.

## Introduction

Computer programs have long been used for
controling the behaviors of machines, but
human activities have not been described in the same style.
Almost all the computers and devices in the whole world
are now going to be connected to the Internet and
controlled by a variety of software written in various programming languages,
but human behaviors and human tasks are not
described in programming language styles, despite the fact that
human task descriptions are often described in similar styles.
For example, cooking recipes resemble programming languages
because they describe the order of tasks that
people should follow for preparing foods.
A recipe for preparing a pasta dish should look like this:

	boil a pan of water
	put some salt
	wait until water is hot enough
	put pasta into boild water
	wait for 10 minutes
	...

Here, a condition statment and a sleep statement is used
in the recipe, just like statements in
conventional programming languages.

After serving the dish, it might be useful to ask people whether
the recipe was good:

    ask people if the pasta tasted good
	
Job instructions can also be described in
program-like manner.
In a conference registration counter, people may be instructed
to work like this:

	while many people are waiting do
	  open all the registration counters
	end

In this way, structure of these instructions are
similar to programming languages, but
computer languages and instructions for humans have been
used in different situations and environments, and they were
not treated as the same thing.

However, the two environments
are getting closer these days, because "crowdsoursing" has been
getting popular.
Many people are working on various research topics where
people can use human resources on the Web
as easily as using software libraries in computing systems.
For example,
users of a new word processor can use a croudsoursing
menu to ask people on the net to rewrite phrases,
just like
running a spell checker on the word processor[Miller].
In this case, there's little difference between
calling a spell checker and asking people on the
Net to rewite sentences.

These approaches are interesting because
distinctions between
computer resources and human resources are diminishing.
However, there still exist big differences between
computer functions and human functions, and
these systems are not flexible enough.
A computer program can get real-world sensing data on the net
using a sensor library,
but it cannot get similar data from people on the net,
since the method of getting data from sensors and
getting information from people are usually very different.
Similarly,
calling a system function and
asking people to do something are quite different.
If we can handle computer systems and people on the net
exactly the same way,
とても面白いことが起こると思われる。

People might like to have a laundry-taking system which can
execute a task like this:

    while true do
      if it's likely to rain then
        take in the laundry
      end
    end

We can use sensor devices or consult the Web to tell if
"it's likely to rain",
but we can also ask people if it is likely to rain or not.
We can use a special robot arm to take in the laundry,
while it would be easier to ask the family member to do the same thing.
In this way, 
either a machine or a human can sense data or perform action
in almost the same way, and
in some cases machines can do the job better than humens,
and in other cases humans are better at the job.

Simple household chores can be specified using
program-like descriptions.
If you have to prepare dinnaer at 19:00, 
you may have to behave like this:

- wash rice at 18:00
- put the rice into a pot with proper amount of water
- wait for 30 minutes
- put the pot on the gas stove with high flame
- set the heat low after hearing the boiling sound
- turn of the gas after 10 minites

Sensing the boiling sound is easy for humans, while simple 
sensing devices cannot detect whether the pot is heated enough.
Waiting for 10 minites is easy for computers, but that is
not easy for humans without using clocks.
For a very simple task like preparing rice,
collabolation between humans and computers is essential.
<!-- センシングは人間がやる -->

While the user is waiting for the rice to be cooked,
he can do other tasks for the meal.
Such activities can be described using a programming language
which supports parallel processing.

## BabaScript

BabaScript is a Node-based programming system that can handle
instructions to humans.

- 人への命令構文ライブラリ
- 人オブジェクトの宣言と基本命令
- オプション情報の付加
- クライアントライブラリ
- 人力リソース管理サービス
- システム利用時の流れ
- 具体的な実装
- 命令プロトコル
- 分散配信
- 特徴

## Examples

### パスタ?
### 実世界ゲーム

## Related works

Many “human computation”[] systems
for integrating computer and human activities have been proposed recently.
Most of them are designed for supporting crowdsourcing activities,
and Amazon's Mechanical Turk[amt] is currently the largest crowdsourcing platform.

<!--
計算機では処理できないようなタスクを解決するために、人を計算資源としてプログラムに組み込む手法はヒューマンコンピュテーション\cite{humancomputation}と呼ばれ、様々な研究が行われている。
米Amazonが運営している AmazonMechanicalTurk\cite{amt} は、クラウドソーシングのためのプラットフォームだ。
mTurk API を通し、人間に対してタスクの実行を依頼することができる。
AUTOMAN\cite{automan}は、crowdprogrammingという概念を唱え、通常のプログラミング言語内でコンピュータによる計算と人による計算を統合した。
CrowdForge\cite{crowdforge}は、MapReduceのような機能をクラウドソーシングのためのフレームワークだ。
クラウドソーシングするタスクを適切に分割し、人力で解かせた後、集合させるといったことができる。
jabberwocky\cite{jabberwocky}は、クラウドソーシングプラットフォームを自由に作れる・再利用できる仕組みをもったDormouseやMapReduce的に人リソースを扱えるManReduce、SQL風のスクリプト言語Dogから構成される、クラウドソーシングのためのフレームワークだ。
CrowdDB\cite{crowddb}では機械だけでは答えられないようなDBへのクエリに対し、クラウドソーシングを使うことで返答させるためのSQLライクなプログラミングを提案している。
CyLog\cite{cylog}はDatalogに似たヒューマンコンピュテーションのためのプログラミング言語だ。
人をデータソースとしてプログラムの中で利用する手法を提案している。
これらの研究は、人を計算資源・データソースとして捉え、コンピュータの代替として人を利用している。
本研究では、人の行動そのものをプログラムとして記述し、実行可能なものにすることを目的としている。

ユビキタスコンピューティングの研究分野においては、Human as Sensor といった概念も存在しており、研究が行われている。
MoboQ\cite{moboq}では、場所ベースのQ\&Aサービスを実装し、その効果を検証した。
Moboqではプラットフォームとしてソーシャルメディアを利用しており、ソーシャルメディア上の人たちをセンサーとして利用している。
スマートフォンを使ったセンシングのためのプラットフォームとしては、PRISM\cite{prism}などが発表されている。
これらの研究では、人をセンサーとして利用し、情報を収集することを目的としている。
本研究では、人の行動をプログラムとして記述することを目的としており、その利用方法はセンサーに限定されたものではない。

人のワークフローを定義するWebサービスとしては、atled\cite{atled}やQuestetra\cite{questetra}などが存在するが、これらのサービスは、人の行動をプログラムで記述するものではない。
BabaScript環境では、人・コンピュータの動作を同一のプログラム上で記述することが可能だ。
-->



## Conclusions

We introduced the BabaSript programing system that can "program"
human behaviors as well as computing behaviors, and showed that
BabaScript is a very good programming framework for
realtime and real-world entertainment environment.
We are planning to use BabaScript for a wide range of
applications, and see the effectiveness.

<!--
  しかしこれらはまだ限定的であり、できないことも多い
   [[[ユーザと機械が対等でない]]]
	ユーザからの 要求に応じて 機械が 動く
	機械からの 要求に応じて 人間が 行動する
   ある時刻にベルをならす(=機械を動)ことはできるが人間を起こす(=人間を行動)ことはできない
   人間のセンサを条件にすることができない
	すごく主観的なものをプログラミングに記述できない
	if 綺麗な景色を見たら then とか
  人間のセンシング行動やアクションも含めて完全に融合したプログラミング環境があれば面白い!
  -->
<!--  
 [[[例]]]
  [[[日常的な仕事の記述]]]
   [[[条件やアクションが人間でも機械でも同等]]]
   [[[if]]] 誰かいる [[[then]]] ドアを開ける
   [[[if]]] 雨がふる [[[then]]] 洗濯をとりこむ
   [[[if]]] 人が足りない [[[then]]] 応援を呼ぶ
   [[[if]]] Amazonが来た [[[then]]] メールする
   [[[if]]] ディスクが無い [[[then]]] 買う(Amazon/アキバ)
   [[[if]]] ビールが無い [[[then]]] 買う
   [[[if]]] 7時になる [[[then]]] 起きる
   7時になったらベルがなるのではなく 7時になったら起きる
   TODOリストとか目覚まし時計とかはプログラミングである
  [[[7時の夕食の用意]]]
   6時に米を洗う
   水と一緒に土鍋に入れて30分放置する
   火をつける
   [[[沸騰したら]]]弱火にする
   8分たったら火を止める
   その間に別の料理を用意する
   この場合、センサを人間がやってる (沸騰したら)
	if文の中身が人間のセンサ
   また並列プログラミングになってる
  [[[既存のシステムではこういう仕事をスクリプトとして記述することはできない]]]
  [[BABAScript]][[[だと楽勝]]]
   だとイイネ
 [[[方法 = プログラム上で人/コンピュータへの命令の区別をなくす]]]
  コンピュータのプログラムと人のプログラムが融合
   行動を人がやる場合と機械がやる場合 (action)
   条件を機械が認識する場合と人が認識する場合 (センサ/条件)
   どちらでも良い場合もある (e.g. 天気)
	「雨がふってきたら」は人間が判断しても機械判断でもよい
  人が得意なことや、人にしかできないことは人にやらせる
   現実のものを動かす
   人間だけが認識できるもの
	CAPTCHAとか
  コンピュータが得意なことはコンピュータにやらせる
   普通の計算とか
   モータを回すとか
  世の中のあらゆる手順や行動をプログラムとして記述する
  人間を機械と同じように記述できる
  
  綺麗な景色だと写真をとる
   みたいなことは人間にしかできない
   -->
  

  