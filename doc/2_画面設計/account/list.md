# 画面項目

## 検索Form

|項目名|input type|対応するイベント|表示制御|
|:-----|:---------|:---------------|:-------|
|社員番号検索|text|-||
|名前検索|text|-||
|管理者権限検索|pulldown|-||
|検索|submit|ユーザ検索||

## Form2

|項目名|input type|対応するイベント|表示制御|
|:-----|:---------|:---------------|:-------|
|管理者権限選択|checkbox||検索後に表示|
|管理者権限変更|submit|管理者情報更新|検索後に表示|
|削除ボタン|button|削除|検索後に表示|

## 削除確認モーダルForm
|項目名|input type|対応するイベント|表示制御|
|:-----|:---------|:---------------|:-------|
|削除|submit|確定||
|キャンセル|button|キャンセル||

## 表示項目

|項目名|output type|対応するイベント|表示制御|
|:-----|:---------|:---------------|:-------|
|社員番号ヘッダ|||検索後に表示|
|名前ヘッダ|||検索後に表示|
|管理者権限ヘッダ|||検索後に表示|
|削除ヘッダ|||検索後に表示|
|社員番号|label||検索後に表示|
|名前|label||検索後に表示|

## 削除確認モーダル表示項目
|項目名|output type|対応するイベント|表示制御|
|:-----|:---------|:---------------|:-------|
|社員番号|label|||
|名前|label|||


# イベント

## 初期表示
account/list.htmlを表示する。

## ユーザ検索
|URI|メソッド|
|:-----|:---------|
|account/list|GET|

### 項目間精査
なし

### 処理内容
以下のサービスを呼び出す。
* S015: ユーザ検索

account/list.htmlを表示する。

## 管理者情報更新
|URI|メソッド|
|:-----|:---------|
|admin/edit|POST|

### 項目間精査
なし

### 処理内容
以下のサービスを呼び出す。
* S009: 管理者情報変更

account/listにリダイレクトする。

## 削除

### 項目間精査
なし

### 処理内容
削除確認モーダル画面を表示する。


## 確定
|URI|メソッド|
|:-----|:---------|
|account/{ID}/delete|POST|

### 項目間精査
なし

### 処理内容
以下のサービスを呼び出す。
* S007: アカウント削除

account/listにリダイレクトする。

## キャンセル

### 項目間精査
なし

### 処理内容
削除確認モーダル画面を閉じる。

