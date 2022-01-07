## 勉強になった

- rack, puma
  - config.ruで設定: nginxの設定ファイルと同じ原理
  - callメソッド準備
  - envの環境変数: リクエスト情報が含まれている

- require
  - 相対パスで指定
  - ファイルを読みこむと内部のクラスを利用できる

- Dir
  - requireを効率よくやる為に為にやっているっぽい
  - Dir[File.join(File.dirname(__FILE__), 'lib', '*.rb')].each{ |file| require file }

- ymlのローディング
  -  YAML.load(File.read(File.join(File.dirname(__FILE__), 'app', 'routes.yml')))

- slim
  - htmlをslimで変換
  - Slim::Template.new(File.join(App.root, 'app', 'views', "#{self.name}", "#{self.action}.slim")) 

- sequel
  - ORMマッパーらしい
  - オブジェクト指向と関係データベースの考え方を上手く変換して繋いでくれるもの
