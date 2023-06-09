# Function callingについて

Function calling の公式の告知は下記のURLを参照してください。  
https://openai.com/blog/function-calling-and-other-api-updates

## Function callingとは
2023/6/13、OpenAI社は新機能「Function calling」を発表しました。公式発表の説明をまとめると次のようになります。 
  
GPT-4-0613とGPT-3.5-turbo-0613の開発者は、これらのモデルに関数を記述し、モデルがそれらの関数を呼び出すための引数を含むJSONオブジェクトをインテリジェントに出力することが可能になりました。これは、GPTの能力を外部ツールやAPIとより確実に連携させる新たな方法です。

これらのモデルは、ユーザーの入力に基づいて関数が必要かどうかを検出し、関数の署名に従ったJSONを応答するように微調整されています。関数呼び出しにより、開発者はモデルからより確実に構造化されたデータを取得できます。例えば、開発者は以下のように利用できます：

- 外部ツールを呼び出すチャットボットの作成。
- 自然言語からのAPI呼び出しやデータベースクエリへの変換。
- テキストからの構造化データの抽出。

これらのユースケースは、新たなAPIパラメータ、functionsとfunction_callを用いて実現され、開発者はJSONスキーマを通じてモデルに関数を記述し、特定の関数を呼び出すことをオプションで指定することができます。

##  本書のどのあたりにからむのか？
主に本書では7章を中心とした説明にからんできます。APIを活用した事例をあげましたが、本書での事例ではGPTモデルに返却する回答をJSON形式として要求をしています。この部分がfunction callingを使用することで大幅に改善することができます。

## まずどのようなものをかを実例で見る
まずは公式で述べられている実例を実行してどのようなものなのかを見てまいりましょう。  
そのためにまずはコードを実行して実際に見ていくのがいいでしょう。LangChainのリポジトリにある次のコードが参考になります。OPEN AIの公式URLの例題をPythonで実装した形になっています。  
https://github.com/gkamradt/langchain-tutorials/blob/main/data_generation/Exploring%20ChatGPT%20Function%20Calling.ipynb  
このURLの記事の中のOpenAI Vanilla Exampleを参照してください。このコードを実行すれば公式の説明が理解できると思います。ですがサンプルではGPT-4を使っているので、一般的ではありません。そこでこのリポジトリでサンプルを参考にしてgpt-3.5-turbo-0613で動くサンプルを作ります。  
これらをGoogle Colabで実行したものをこのディレクトリにおいておきますので、インポートをして実行してみてください。  
[fuction_calling_01.ipynb](https://github.com/gamasenninn/gihyo-ChatGPT/blob/main/additional_topics/function_calling/fuction_calling_01.ipynb)

## 7章のユースケースをFunction callingを使った場合どうなるか
（未実装・作業中）



