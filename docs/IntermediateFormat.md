# UI構造の中間表現フォーマット

PoCではJSONベースのフォーマットを採用します。基本構造は以下のとおりです。

```json
{
  "screens": [
    {
      "id": "screen1",
      "name": "ログイン画面",
      "components": [
        {"type": "text", "id": "title1", "value": "ログイン"},
        {"type": "text_input", "id": "user", "placeholder": "ユーザー名"},
        {"type": "text_input", "id": "pass", "placeholder": "パスワード"},
        {"type": "button", "id": "submit", "label": "送信"}
      ]
    }
  ]
}
```

各コンポーネントには`id`と`type`を必須とし、必要に応じて`props`オブジェクトで詳細を表現します。
