## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
  * エンドポイント：https://zipcloud.ibsnet.co.jp/api/search  
    機能：日本の郵便番号を入力することで、それに対応した住所情報を検索することができる。  
* リクエストとレスポンスのフォーマット
 * リクエスト：http://zipcloud.ibsnet.co.jp/api/search?zipcode={調べたい郵便番号}  
   レスポンス：{ "message": null, "results": [ { "address1": "県名", "address2": "市名", "address3": "町名", "kana1": "県名フリガナ", "kana2": "市名フリガナ", "kana3": "町名フリガナ", "prefcode": "都道府県コード", "zipcode": "調べたい郵便番号" } ], "status": APIのステータスコード }  
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
  * 名称：気象庁のAPI  
  * 参考URL：https://anko.education/webapi/jma  
* エンドポイントと機能
  * エンドポイント：https://www.jma.go.jp/bosai/forecast/data/overview_forecast/130000.json  
  * 機能：天気予報の概要を取得する。  
* リクエストとレスポンスのフォーマット
  * リクエスト：
    https://www.jma.go.jp/bosai/forecast/data/overview_forecast/{地域コード}.json  
  * レスポンス：{"publishingOffice":"気象庁","reportDatetime":"予報の発表日時","targetArea":"予報地点","headlineText":"","text":"予報テキスト文"}  
### Q3-3. 感想
* 今回の課題で苦労したこと
  * kadai5-1で、入力した郵便番号をリクエスト文にどのように含めればいいのかわからず、試行錯誤したこと。  
* 演習を通して理解できたこと
  * APIには便利なものから面白いものまでさまざまな種類が提供されていて、容易にWebページに組み込むことが可能であるとわかった。  
* Web APIの利便性や課題など
  * WebAPIは他のサービスを容易にシステムに組み込むことができてとても便利なものであるが、その手軽さにより悪意を持った攻撃に悪用されやすい仕組みだと思うため、信頼のできるWebページか、信頼のできるAPIの提供先かどうかを見極めて使用していく必要があると感じた。
