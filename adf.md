# Tips

## InputTextでEnterキー押下時に検索を実行

1. 対象のInputTextの属性変更

		autoSubmit = true

2. レンダリング対象のPartialTriggersにInputTextを指定（autoSubmitはPartialSubmitとなるため。）

3. Form(af:form)の属性変更

		DefaultCommand = searchButton

## ActionListenerの処理後にビューを更新

PartialSubmitとして送信されるため、更新対象のコンポーネントのPartialTriggers属性へイベント発信源コンポーネントを登録する。
なお更新対象のコンポーネントにコンテナ系コンポーネントを選んだ場合は子要素すべてが更新される。

