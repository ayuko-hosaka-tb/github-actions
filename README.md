# github-actions

[![backend](https://github.com/ayuko-hosaka-tb/github-actions/actions/workflows/backend.yml/badge.svg)](https://github.com/ayuko-hosaka-tb/github-actions/actions/workflows/backend.yml)

## サンプルアプリケーション

静的なフロントエンドと Web API から成る、足し算アプリケーションです。

## 1.開発モードで起動する

サンプルアプリケーションは、以下の手順で開発モードで起動します。

```
cd backend/
npm run dev
```

以下のレスポンスが返ってきたら
ブラウザで http://localhost:80 にアクセスしてください。

```
Sample app listening on port 80
```

## 2.テストコードを実行する

テストコード src/sum.test.ts を実行する場合、以下のコマンドを実行してください。

```
cd backend
npm run test
```

以下のレスポンスが帰ってきたらテスト実行は成功です。

```
 PASS  src/sum.test.ts
  √ apps 1 + 2 to equal 3 (4 ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        1.424 s, estimated 2 s
Ran all test suites.
```

## 3.バックエンドをビルドする

バックエンドをビルドして実行する場合は、以下のコマンドを実行してください。

```
cd backend/
npm run build
```

以下のレスポンスが返ってくると backend 直下に dist/index.js が生成されます。

```
> backend@1.0.0 build
> ncc build

ncc: Version 0.36.0
ncc: Compiling file index.js into CJS
ncc: Using typescript@4.9.5 (local user-provided)
944kB  dist\index.js
944kB  [2218ms] - ncc 0.36.0
```

## 4. dist/index.js を実行する

以下のコマンドを実行してください。

```
cd backend
node dist/index.js
```

以下のレスポンスが返ってきたら
ブラウザで http://localhost:80 にアクセスしてください。

```
Sample app listening on port 80
```
