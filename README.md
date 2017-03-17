# useful-daily-report

> Java開発研修（新人向け、4週間@6月）では、Javaに関する基本的な講義を受けつつ、演習形式で本システムを作成する。

# システム方針（エレベータピッチ）
* 後続研修（７～８月）の新人 向けの、
* 日報システム というプロダクトは、
* 日報としての使いやすさを追い求めたWebアプリケーション です。
* これは SNSのように他の人の日報がタイムラインで見られ、コメントをすることが でき、
* 無理やりベンダーのLMS（学習管理システム）を利用して日報を書くの とは違って、
* 他者とコミュニケーションを円滑に行える仕組み が備わっている。

# システムアーキテクチャ
* FW : Spring Boot(Spring MVC)
* View : JSP
* DB : Oracle

# 機能要件
## 機能一覧

|業務|機能|備考|学習できる技術要素(ﾒｲﾝﾀｰｹﾞｯﾄはJava)
|---|---|---|---
|日報|タイムライン|•ユーザが投稿した日報を新着順に、SNSのタイムライン形式で一覧表示する。<br>•自分が登録した日報をフィルターすることができる。<br>•ホーム画面。
|日報|日報投稿|•日報を投稿する。<br>•研修の満足度、満足度理由を投稿する。
|日報|日報内容|•タイムラインで選択した日報の内容を表示する。<br>•コメント入力、表示機能を備える。<br>•自分が投稿者であれば、編集画面に遷移することができる。
|日報|日報編集|•日報を編集する。
|日報|日報検索|•投稿日、投稿者、ワード等で日報を検索し、検索条件に当てはまった日報を一覧表示する。

## 機能一覧（内部）

|業務|機能|備考
|---|---|---
|ユーザ管理|ユーザ登録|•ユーザ名、パスワードを登録する。
|ユーザ管理|ログイン|•登録されたユーザ、パスワードでログインする。

## 機能一覧（発展）

|業務|機能|備考|学習できる技術要素(ﾒｲﾝﾀｰｹﾞｯﾄはJava)
|---|---|---|---
|日報|友達機能|•タイムラインに、友達フィルター機能を追加する。|
|ｺﾐｭﾆｹｰｼｮﾝ|チャット|•ユーザ同士が１対１でチャットする。|
|ｺﾐｭﾆｹｰｼｮﾝ|掲示板|•講師に仕事について質問する掲示板。|
|研修分析|満足度集計結果|•その日時点での満足度集計結果を表示する。<br>•テーマごとの満足度が分かる。|
|研修分析|ﾃｷｽﾄﾏｲﾆﾝｸﾞ|•頻出コメントを一覧化する。|
|ユーザ管理|認可|•研修分析は、管理者ユーザしか操作閲覧できない。|
