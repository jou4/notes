% ADF
% K.Kamitsukasa
% 

# Tips

## InputTextでEnterキー押下時に検索を実行

1. 対象のInputTextの属性変更

		autoSubmit = true

2. レンダリング対象のPartialTriggersにInputTextを指定

	* autoSubmitはPartialSubmitとなるため。

3. Form(af:form)の属性変更

		DefaultCommand = searchButton
