# README
# アプリケーション名  
cheat  
# アプリケーション概要  
1日1日の食べたいものを写真付きで記録し週１のなんでも食べられる日に後悔のないチートデイを実行することができる  
# URL  
  
# テスト用アカウント  
  
  
  
  
# 利用方法  
1.トップページからユーザー新規登録を行う  
2.投稿ボタンから(タイトル、画像)を入力し投稿する
3.チートデイが終了したら削除ボタンを押す  
# アプリケーションを作成した背景  
普段から食事の節性を行っており週に１回だけ好きなものを好きなだけ食べていいチートデイを設けています。  
実際にチートデイを迎えた問題点は何を食べたかったか曖昧になってしまい、その日の気分で物を食べてしまうということが多々ありました。  
このアプリを作ることによって明確な目標ができ、日々の節制のフラストレーション解消にも繋がると思い開発することにしました。  
# データベース設計  
[![Image from Gyazo](https://i.gyazo.com/345008707f358ce0aed699c910d8aa41.png)](https://gyazo.com/345008707f358ce0aed699c910d8aa41)  
# 画面遷移図  
[![Image from Gyazo](https://i.gyazo.com/1ebff3d3a9939619c0e9d6e67ab54e39.png)](https://gyazo.com/1ebff3d3a9939619c0e9d6e67ab54e39)  
# users テーブル  
| Column                 | Type   | Options     |
| ---------------------- | ------ | ----------- |
| nickname               | string | null: false |
| email                  | string | null: false, unique: true, |
| encrypted_password     | string | null: false |  
# Association  
has_many :cheats  
# cheats テーブル  
| Column                 | Type   | Options     |
| ---------------------- | ------ | ----------- |
| food_name              | string | null: false |
| user                   | references ｜ null: false,foreign_key: true |  
# Association  
belongs_to :user  
# 開発環境  
HTML.CSS.RUBY.テキストエディタ  
# ローカルでの動作方法  
  
  
# 工夫したポイント　  

