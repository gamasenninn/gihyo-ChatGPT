#  Code Interpreterについて

2023/7/8、GPT Plusユーザ限定でCode Interpreterが使用できるようになりました。
以下はOpenAI社の公式ツイートです。  
```
Code Interpreter will be available to all ChatGPT Plus users over the next week.
It lets ChatGPT run code, optionally with access to files you've uploaded. You can ask ChatGPT to analyze data, create charts, edit files, perform math, etc.
Plus users can opt in via settings.

Code Interpreter は来週中にすべての ChatGPT Plus ユーザが利用できるようになります。
これはChatGPTにコードを実行させるもので、アップロードしたファイルにアクセスすることもできます。ChatGPTにデータ解析、グラフ作成、ファイル編集、計算などを依頼することができます。
Plusユーザーは設定からオプトインできます。
```
これを受け、本書との関連を補足説明をします。
##  本書のどのあたりにからむのか？
主に本書では9章を中心とした説明と関係します。LangChain特にAgentを活用した事例をあげましたが、質問文から自動でpythonコードを生成し、実行し結果を出力する処理です。これらの処理がCode Interpreterを使うことで同じことができます。

## Code Interpreterの実例
論より証拠。実例を見ていきましょう。  
### 数独パズルを解く例
最も簡単な例として9-5の数独パズルを解く例です。  
次のように簡単な質問文で数独の問題の2次元配列を渡します。  
すると、自動的にpythonコードが作成されそれを実行し、回答を表示します。  

![数独パズルを解く例](./images/ci_sudoku.jpg)

### パワーポイントの自動生成 (9-4)
9-4で示した自動的にパワーポイントファイルを生成する例を試してみましょう。

![企画書草案を提案](./images/pptx01.PNG)
![企画書草案を提案](./images/pptx02.PNG)
![企画書草案を生成](./images/pptx03.PNG)
  
kikaku.pptxがダウンロードできるようになっています。  
クリックしてダウンロードし、ファイルを開くと次のように企画書の草案が出来ています。  
  
![PPTXファイルを開く](./images/pptx04.PNG)

### diagramsによるクラウド図の自動生成 (9-4)
diagramsライブラリーはCode Interpreterに搭載されたPython環境にはインストールされていないようです。それをインストールには外部からネットワークを経由する必要があり、その場合はインストールを行わないと判断するようです。

![diagrams](./images/diagrams.PNG)


### グラフの自動生成 (9-4)
グラフの自動生成はCode Interpreterの得意とするところです。

![graph01](./images/graph01.PNG)
![graph01](./images/graph02.PNG)
  
  
![graph01](./images/graph03.PNG)

### 分野別の学習(6-1)  
Code Interpreterを使うことで、分野別学習が飛躍的に効率がよくなります。  
たとえば苦手な数学分野などに応用ができるのではないでしょうか。たとえば、方程式を解くことが簡単にできるようになりました。もちろん行列式なども解くことができます。  
また、分野を特定しサンプルの方程式を出力してもらい、そのグラフを描いてもらったりすると理解が深まります。

![math01](./images/math01.PNG)
![math01](./images/math02.PNG)
![math01](./images/math03.PNG)

### TDD with ChatGPT....テストコードの実行(5-2)  

書籍ではまずテストコードを書いて、その後ChatGPTにコード生成を依頼するという形を説明しています。Code Interpreterを使うことで、テストの実行をChatGPTのUI上で完結することができます。これはとても画期的です。  
  
さらに応用的にな使いかたもできます。  
テストコードと本体関数を同時に生成、テストコードを実行してもらうことです。
テストコードが一発で通らない場合は、何度もリトライしてテストコードが通るまで実行してくれる、というのが大きなポイントです。  

![test01](./images/test_code01.jpg)
![test02](./images/test_code02.jpg)
![test03](./images/test_code03.jpg)

## グラフの表示で日本語が化ける問題への対処

Code Interpreterで出力されるグラフは日本語に対応していません。  
タイトルや軸ラベル、凡例など日本語表示が必要な場合は、別途日本語フォントファイルをアップロードする必要があります。  
例として、IPAフォントを使いたい場合、次のサイトからフォントファイルをダウンロードして使いたいフォントをアップロードします。  
[IPAフォントのダウンロードサイト](https://moji.or.jp/ipafont/ipafontdownload/)  
  
次の例ではipaexg.ttfをアップロードし、プロンプトにそれを使用するように指示してサンプルグラフを描いてもらったものです。
![font01](./images/font01.png)  
![font02](./images/font02.png)  
もちろん、フォントファイルのアップロードはグラフ作成プロンプトとは別にあらかじめ指示しても問題ありません。  
うまくいかない場合は、フォントファイル名を明確に指示してください。


## ファイルをアップロードして解析してもらう


  
（以下、追加説明掲載予定）
