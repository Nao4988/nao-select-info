# Nao Select Privacy Policy
# Nao Select プライバシーポリシー

発効日：2026年9月17日

最終更新日：2026年9月17日

本ポリシーは、Nao Select（以下「本ツール」）における情報の取扱いを説明するものです。本ポリシーは日本語を正文とします。

## 1. サービス概要

本ツールは、Pinterestビジネスアカウントの所有者本人が使用する、商品紹介コンテンツの管理を目的としたローカルツールです。Pin投稿案の準備、Board管理、利用者が明示的に選択したPinの投稿、投稿管理、および許可された範囲でのPinterest Analytics確認を目的としています。

本ツールは現在、個人利用を前提とした開発・検証段階です。Pinterest APIへの実接続を伴う機能は、Pinterestのアクセス承認、適用規約、および本ツール内のSafety Gateを満たした場合に限り使用します。現在のローカル検証はdry-runを標準としています。

## 2. Pinterestとの連携

本ツールがPinterestと連携する場合は、Pinterest APIならびにPinterestが提供するaccess tokenまたはOAuth等の正式な認証方式のみを使用します。

本ツールは、次の情報を要求または取得しません。

- Pinterestのパスワード
- Pinterestのsession cookie
- その他のPinterestログイン認証情報

本ツールは、利用者が認識していない状態でPinterestアカウントを操作することを目的とせず、投稿等の操作には対象ごとの確認とSafety Gateを設けます。

## 3. 処理する可能性がある情報

本ツールは、機能提供に必要な最小限の範囲で、次の情報を処理する可能性があります。

- Pinterestアカウントの所有者が認可した情報
- BoardおよびPinの操作に必要な情報
- Pinterestが利用を許可したPin performanceまたはAnalytics情報
- 利用者自身が本ツールへ入力・編集した投稿案
- 利用者が登録した楽天ROOM URL
- 商品候補、投稿状態、およびローカル操作履歴

Pinterest APIから取得した情報は、Pinterest Developer Guidelinesその他の適用規約で明確に許可される範囲を超えて永続保存しません。保存可否が明確でない情報については保存せず、必要な場合にAPIから取得する設計とします。

## 4. API Credentials

Pinterest access token、App Secret、refresh tokenその他の認証上の秘密情報は、利用者のローカル環境で管理します。これらを公開GitHub Repository、公開文書、データベース、通常ログ、または認証済みrequest URLへ保存・出力しません。

本ツールは、API credentialsを第三者に販売または共有しません。

## 5. AIの利用

現時点では、Pinterest APIから取得したデータをOpenAIその他の第三者AIサービスへ送信しません。Nao Select内部でAIを利用する機能がある場合も、Pinterest API由来データとの処理境界を分離します。

将来この取扱いを変更する場合は、適用されるPinterestの規約およびプライバシー上の要件を事前に確認し、必要に応じて本ポリシーを更新します。

## 6. 楽天関連サービスとの関係

本ツールは、楽天市場や楽天ROOMに関連する商品候補、URL、利用者が作成した投稿案を扱う場合があります。ただし、Pinterest APIから取得したデータを楽天その他の第三者サービスへ共有または販売しません。

楽天ROOMへの投稿は、現在、利用者本人が手動で行います。本ツールは楽天ROOMの自動投稿やブラウザ自動操作を行いません。

## 7. 利用目的

本ツールが情報を処理する目的は、次のものに限定します。

- 利用者本人のPinterest投稿管理
- Board管理
- Pinの準備および作成
- 投稿状況の確認
- Pinterestが許可したAnalyticsの確認
- 本ツールの機能提供および改善
- セキュリティ確保および障害診断

これらの目的を超えてPinterest API由来データを利用しません。

## 8. 第三者提供

本ツールは、Pinterest API由来データを第三者へ販売しません。広告データブローカーその他の第三者へ提供せず、Pinterest Developer Guidelinesで許可されない他サービスの情報との結合を行いません。

法令上必要な場合を除き、Pinterest API由来データをアカウント所有者以外へ共有しません。

## 9. 保存期間

利用者が入力した投稿案、ROOM URL、承認状態、操作履歴など、Nao Select自身が生成・管理するローカルデータは、本ツールの機能提供に必要な期間のみ保存します。

Pinterest API由来データは、Pinterest Developer Guidelinesその他の適用規約で保存が明確に許可される範囲に限定します。永続保存が許可されない情報は、必要時にAPIから取得し、不要になった後は保持しません。保存可否の確認が完了していないPinterest API由来情報は、永続保存しない方針です。

## 10. 利用者による管理

利用者は、次の方法により連携やローカルデータを管理できます。

- Pinterestの設定からアプリ連携を解除する
- Pinterest access tokenを失効させる
- Nao Selectのローカルデータを削除する

連携解除またはtoken失効後は、その認証情報を使用した新たなPinterest APIアクセスを行いません。

## 11. セキュリティ

本ツールでは、次のような措置を講じます。

- Secretsを公開Repositoryへ保存しない
- 認証情報や認証済みrequest URLをログへ出力しない
- ローカル利用ではlocalhost接続を基本とする
- Pinterest Production操作にSafety Gateを設ける
- APIエラー、認証エラー、データ形式不正時はFail-closedとする

これらはリスクを低減するための措置であり、完全な安全を保証するものではありません。

## 12. 子どもの利用

本ツールは、13歳未満の子どもを対象としたサービスではありません。

## 13. 本ポリシーの変更

本ツールの機能、利用する外部サービス、法令、または適用規約の変更に応じて、本ポリシーを変更する場合があります。重要な変更がある場合は、この公開ページを更新します。

## 14. お問い合わせ

本ポリシーに関する問い合わせは、次の公開Repositoryをご利用ください。

https://github.com/Nao4988/nao-select-info

公開Issueには、access token、App Secret、パスワード、個人情報、その他の秘密情報を投稿しないでください。

## English summary

Nao Select is a local, owner-operated tool under development for preparing and managing product-related Pinterest content. It uses only Pinterest-authorized API authentication methods and does not request Pinterest passwords or session cookies. Pinterest API data is not sold, shared with third parties, sent to external AI services, or persistently stored beyond what Pinterest rules clearly permit. API credentials remain local and must never be committed to a public repository. Users can revoke Pinterest access and delete local Nao Select data. This English summary is provided for convenience; the Japanese text controls.
