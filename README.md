test1

# gihyo-ChatGPT
このレポジトリは技術評論社刊「ソフトウェア開発にChatGPTは使えるのか？」のサポートレポジトリです。  
書籍で使用したコードや、出版後発覚した正誤表、追加すべき補足説明などこのリポジトリでサポートをします。出版後に発表された新技術のトピックスなどもキャッチアップします。  
また、読者様から寄せられたさまざまな意見をもとにISSUEを切り、番外編として記事およびそのソースコードなどを追加していく予定です。

## コードサンプルの場所

[notebooks](./notebooks/)に書籍で使用したコードを保存してあります。
Google Colab上で動作するものです。

## 出版後のトピックについて
出版後に出たトピックをここでキャッチアップしていく予定です。
- Function Calling  
2023/6/3にAPIの仕様でfunction callingが追加されました。これによって、より便利にAPIが使えるようになりました。特にJSON形式で返却を期待するアプリケーションはより便利になります。このトピックに関しては、[additional_topics/function_calling](./additional_topics/function_calling/)を参照してください。

- Code Interpreter  
2023/7/8日本のGPT Plusユーザ限定でCode Interpreterが公開されました。ChatGPTのGPT-4ユーザーインターフェースで質問から自動的にコードを作成し実行、結果を表示するといったことができるようになりました。またファイルをアップロードしそれをもとに解析、解析結果の表示やグラフ表示ができます。これは強力な機能です。このトピックに関しては
[additional_topics/Code_Interpreter](./additional_topics/Code_Interpreter/)を参照してください。

## 正誤表について
出版後に発覚した間違い、補足説明・補足注釈については[正誤表としてERRATA.md](./ERRATA.md)に挙げていく予定です。
