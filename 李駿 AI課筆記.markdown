# 李駿AI課

先從定義開始：
什麼是智能? What is intelligence?
能完成複雜目標的能力！包含3個範疇：

> 感知
> 思維：學習 (試錯學習)、推理
> 行為：無意識自動化行動

AI: Non-biological intelligence
非生物學上的智能。
從生命3.0 書中擷取的概念來看，智能是指具有感知，推理，預測的能力，必且具有能達成複雜任務的能力。

Narrow intelligence: 僅能達成某個特定任務的人工智能

General intelligence: 能達成任何形式的目標，**尤其包含學習在內**。遊戲或者影視作品裏頭指稱的就是這一類人工智能(Artificial general intelligence，AGI，又名 Human level AI或者 Strong AI)。而學習的能力，是人類十分特殊且可以迭代改善的能力。

Superintelligence: 遠超人類的general inteligence。

Intelligence explosion: 智能爆炸，或者用借代物理學上的奇異點(Singularity)，表達科技的爆發可能更容易為人理解這個詞的意思。
一張圖代表AI達成任務的難易度里程碑

### 人工智能的發展史:

最早在1943年神經網絡就已經被提出了。而1950年圖靈測試被提出來。1956年達特茅斯會議中，一群當時計算機的研究者會聚在一起討論以及提出各式觀點。
1958年，有了兩個流派的發展路線，第一個 The Neats(簡約派)，由John McCarthy等人提出，強調的是不需要讓計算機與人類有著同樣的思考方式，只要能解決、回答我們人類的問題就好了，它需要的就是規則、邏輯、專家系統，或者用窮舉的方式解決問題；另一方面，由Marvin Minsky等人提出的則是更接近人的思維框架，The Scruffies，期待藉由類似於人的推理能力，達到解決問題的目的。當時由於計算力的不足，The Neats並沒有如同現在般占優勢。大約在1980年代之後，由於算力的大幅精進(積體電路的發明)，與之相關的神經網絡再次引起了注意。

在1988年以後引入了更多的其他學科的概念，包含概率論和決策理論，如貝葉斯網絡，隱馬爾可夫模型，信息論，隨機模型和經典優化理論等等。
直到1997年，IBM的深藍電腦與前蘇聯Gary Kasparov下國際象棋的獲勝成為一個標誌性里程碑，而其算力為最初Ferranti Mk1的一千萬倍。

2010年由於移動網絡，移動計算機的出現，一下子許多人都有了可供隨時使用的計算機，尤其是智能手機帶來的巨大影響。因此，幾乎是一瞬間網絡上的數據出現了近一步爆炸性的增長。這一點如同笑來老師說過的，梅特卡夫定律：節點的價值與節點數量的平方成正比！
2022/12/04 00:33:50

### 為什麼特別會用國際象棋這一類遊戲當示範呢？

這是計算機最擅長的能力，藉由全信息的環境去做計算，換句話說是這樣的"學習環境"，屬於友好學習環境。

接下來的遊戲人工智能的發展，會踏入那些具有信息不對稱的博弈，比如英雄聯盟、星海爭霸等等。這一類較不友善的學習環境，對現有人工智能的挑戰比較大。

### 圖像識別
ImageNet Classification Error (Top 5)：

<img src="https://seeme.ai/img/blog/deep-learning-a-definition/Winner-results-of-the-ImageNet-large-scale-visual-recognition-challenge-LSVRC-of-the.png">

### 語音識別
Speech Recognition Word Error Rate (WER)

### 機器翻譯
是自然語言裡頭較為困難的領域。就算是人類，那怕是懂雙語的，要做到信、達、雅的翻譯，也是很困難的，大部分人是做不到的。
不過目前對人工智能的要求是，能理解內容即可。

## 計算、算法、資料

CPU對浮點運算的效能不如GPU，後者在這一點上的效能是前者的千倍到萬倍。
後來在大約2010年後，由於研究者發現人工智能的計算主要也是浮點數運算，因此GPU就被拿來用在人工智的計算基石。換句話說，人工智能的計算力只因為這一個變動，算力就提升了千倍萬倍，相當驚人。

# 機器學習
近期最熱門的機器學習，是過往人工神經網絡的再推出。此架構試圖模擬生物的大腦神經網絡資訊流的處理過程。

### MNIST (Modified National institute of Standards and Technology database)

目前是機器學習的入門主要從視覺圖像辨識開始。MNIST作為基礎資料庫，可用來訓練算法，而得到基礎的圖像識別能力。

## 神經網絡的架構

以MNIST的資料庫為例，每張圖有28 x 28 = 784 像素。
先決定好輸入層(input layer)、輸出層(output layer)。
接者決定中間層的層數以及其中的個數，通常稱為The hidden layer。究竟需要多少層或者其中所含的"細胞個數"，看個人調控。關鍵點是，**上一層的每一個神經元都要連接到這一層的每個細胞**。

> input layer
>
> The Hidden layer
>
> Output layer

而中間層的神經元根據某個公式，比如示範中的：

$$ b_{i} = w_{1}a_{1} + w_{2}a_{2} + w_{3}a_{3} + ... + w_{n}a_{n}$$

或者我們可以用一個bias的數做參數調整：

$$ b_{i} = w_{1}a_{1} + w_{2}a_{2} + w_{3}a_{3} + ... + w_{n}a_{n} - b $$

又或者可以加總起來：

$$ b_{i} = \sigma(w_{1}a_{1} + w_{2}a_{2} + w_{3}a_{3} + ... + w_{n}a_{n} - b) $$

講到這裡，那麼所謂的機器學習到底是什麼呢？就是藉由這三層在檔案庫的回饋下，自動計算那些裡頭調控的參數，直到其回答問題的答案正確慮到一定精確度。某種程度上，這種方式是讓算法自己大量試錯後，得到較為正確得流程。最大的好處是，不需要人類自己把每個參數做調整。

那麼，人類在其中的角色是什麼呢？ 幫助參數的調節與算法的穩定。

Deep learning 可區分成兩階段：
1. Training/ learning，應用訓練集 (traning data set)找到最好的 weight 與 bias。

2. Application，則是運用已經調整好訓練好的AI。

#### Training 的手法
* Supervised Learning(有監督的學習): training set is labeled (模擬題有標準答案)
* Unsupervised Learning: training set is not labeled (模擬題沒有標準答案，但是我把訓練集做一些分析推測，接著反過來做修正參數)
* Reinforcement Learning(強化學習): training is a sequence of trial and reaction (trial and feedback，有點聽不懂)。這個學習的方式跟前面兩個不同，只會提供相較於真實答案，算法得出的答案究竟是高了還是低了的回饋。

與標準答案的差距，稱為**the losses**。接著回過頭讓機器調整據此調整參數。
反向傳播：怎麼通過 losses 去反過來優化算法，幫助神經網絡更快找到高效的穩定網絡算法。

回過頭來看，運用MNIST訓練的算法，其錯誤率(Error rate)可以達到[低於1%的程度](https://en.wikipedia.org/wiki/MNIST_database)。

## 當前主流機器學習框架: TensorFlow (google)與 Pytorch(facebook)
### TensorFlow
比較適合於部屬在生產環境；而PyTorch比較適合在研究環境中。

2022/12/05 1:17:41

## 當前流行的領域方向
Computer Vision 計算機視覺
>   Recognition
>
>   Construction
>
>   Image Understading
>
Natural Language Processing (NLP) 自然語言處理
>   Syntax
>
>   Sematics
>
>   Discourse (寫個 Summary)
>
>   Speech (相對簡單一些，把語音識別成文字，把文字識別成語音)
>
>   Dialog (對話系統)
>
Decision mMaking (決策)
>   Gaming (競爭遊戲)
>   
>Investment
>
>   Business Strategy

再次強調參考書 Life 3.0
另一個初步參考資料是李駿老師寫的[Cyborg和人類的進化](https://soulhacker.me/posts/the-evolution/)

最後用Jupyter lab 開啟 Tensorflow 演示機器學習的組件化與模塊化部分，需要且值得多看幾遍。

