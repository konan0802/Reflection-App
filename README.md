# Reflection App
チャット形式で日々の振り返りを行うためのiOSアプリ

## DEMO
<img src="ui.png" width="350px">

[Figma](https://www.figma.com/file/Hoqn0h6B3zDAGtcRuOfQGm/YWTReview?node-id=0%3A1)

## Features
* 「EASN」という日々の経験から自己を振り返るフォーマットを利用
* iOS(iPhone SE3, iPad mini6)とWebに対応しているため場所や時間を選ばずに入力が可能
* （今後は）対話形式のUIに変更して、より”振り返り”の心理的ハードルを下げる

### ◇EASN
* E（経験）
    * 具体的な経験
    * 成功,失敗に関わらず特徴的な経験
* A（行動）
    * 行動レベルの振り返り
    * その経験に際してどのような行動を取っていたか？
    * これまではどのような行動を取っていたか？
* S（スタンス）
    * スタンスレベルの振り返り
    * その行動の前提としてある自身のスタンスは何か？
    * 何を感じて、考えて、その行動を取っていることが多いか？
* N（ネクストアクション）
    * スタンスを鑑みた上での次回の打開行動
    * スタンスは自身の本質でもあるため蔑ろや否定は行わない
    * 失敗の経験であれば改善行動、成功の経験であれば転用可能な事柄

※ 開発者が独自に提唱している振り返りフォーマットです

## Architecture
### ◇FE
* Flutter
### ◇BE
* Golang
### ◇DB
* DynamoDB
### ◇Infra
* Lambda
* API Gateway
* Cognito

<img src="drawio.png" width="500px">

## Deploy
### ◇ BE
1. **ECRへのプッシュ**<br>
    ⇒ ECRのプッシュコマンドを参考
2. **Lambdaへのデプロイ**<br>
    ⇒ イメージタブの［新しいイメージをデプロイ］を押下

## Ref
* [AWS Lambda+API Gateway+DynamoDBでCRUD APIを作るのをGolangでやってみた](https://qiita.com/saki-engineering/items/e5cf56301d94ceea3ce0)
* [Cognito でサインアップしたユーザーの情報を DynamoDB に保存するには？](https://zenn.dev/tatsurom/articles/cognito-data-to-dynamodb)
* [Providerで状態管理](https://www.flutter-study.dev/firebase-app/provider)
* [プログラミングせずにCognitoで新規ユーザー登録＆サインインを試してみる](https://dev.classmethod.jp/articles/sign-up-and-sign-in-by-cognito-with-awscli/)
* [FlutterとAmazon Cognitoでログイン機能を実装してみた](https://dev.classmethod.jp/articles/flutter-cognito/)