# Learning Flutter
Flutter学習用のリポジトリ

## Setup

### Android
1. Android Studioを入れておく
2. Android Studio内でFlutter Pluginをインストール
3. Preferences > Editor > Code Style > Dartからdartfmtを使用するようにチェックを入れておく

### iOS
1. Xcodeを入れておく

### Flutter SDK
1. https://flutter.io/docs/get-started/install/macos
    * これに沿っていろいろ設定
    
### コードフォーマットの設定
* https://qiita.com/kazuki229/items/bb26e50825cf8a739888

## 参考URL

### 読み物
* [iOSネイティブアプリ開発者から見たFlutter 2018年8月 Release Preview 1 時点での所感](https://medium.com/flutter-jp/flutter-ios-5b2178018d3e)
* [Flutterの効率良い学び方](https://medium.com/flutter-jp/flutter-learning-c5640c5f05b9)

### 手を動かすのによさそうなやつ
* [Flutter Docs](https://flutter.io/docs)
    * 公式のドキュメント。とにかく豊富
* [Flutter samples](https://github.com/flutter/samples/blob/master/INDEX.md)
    * アーキテクチャのサンプリなどもリンクされている
* [cookbook](https://flutter.io/docs/cookbook)
    * 逆引き的なやつ
* [codelabs](https://flutter.io/docs/codelabs)
    * codelab。いくつかある
* [Dart and Flutter: The Complete Developer's Guide](https://www.udemy.com/dart-and-flutter-the-complete-developers-guide/learn/v4/overview)
    * Udemy

### ライブラリ
* [simple_logger](https://pub.dartlang.org/packages/simple_logger)
   * コードジャンプできるようになっているLoggerライブラリ
   * https://medium.com/flutter-jp/logger-ec25d8dd179a

* [spritewidget](https://pub.dartlang.org/packages/spritewidget)
   * 2Dゲーム作成用のライブラリ
   * https://github.com/spritewidget/spritewidget

## メモ

### Dart

#### アクセス修飾子
Datrではプレフィックスとして `_` をつけると、そのクラスに対してprivateになる。

### Flutter

#### 外部パッケージ(ライブラリ)の追加
1. pubspec.yamlを編集
2. `flutter packages get` を実行

#### Stateless widget
Stateless widgetはimmutable。  
すべてのプロパティはfinalであり、変更できなくなっている。  
(Javaのfinalと同じなら、再代入ができないだけでimmutableということではなさそう？要検証)  

#### Statefull widget
変更される可能性のある状態を保持しておけるWidget。  
実装するには次の2つのクラスを使う。  
1. [StatefulWidget class](https://docs.flutter.io/flutter/widgets/StatefulWidget-class.html)
2. [State<T extends StatefulWidget> class](https://docs.flutter.io/flutter/widgets/State-class.html)
   
#### ListView
リストビュー。Androidで言うRecyclerViewみたいなやつ。  
itemBuilderに各要素の表示内容を記述する。  

#### ListTile.divideTiles
各要素に区切り線を追加してくれるメソッド。

#### ListTile
シンプルなリスト表示に使えそうなWidget。

#### Navigator
画面遷移に使うやつ。  
Flutter的には `Route` を追加するというらしい。
`Navigator.of(context).push(...)` で次の画面へ遷移する。  
遷移後の画面にはアップボタンが自動的に追加される。  

#### Row
子供のウィジェットを水平方向へ並べる
