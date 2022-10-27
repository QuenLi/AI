# 李駿AI課
AI: Non-biological intelligence
從生命3.0 書中擷取的概念來看，智能是指具有感知，推理，預測的能力，必且具有能達成複雜任務的能力。

Narrow intelligence: 僅能達成某個特定任務的人工智能

General intelligence: 能達成任何形式的目標，包含學習在內。遊戲或者影視作品裏頭指稱的就是這一類人工智能(Artificial general intelligence，AGI，又名 Human level AI或者 Strong AI)。而學習的能力，是人類十分特殊且可以迭代改善的能力。

Superintelligence: 遠超人類的general inteligence。

Intelligence explosion: 智能爆炸，或者用借代物理學上的奇異點表達科技的爆發可能更容易為人理解這個詞的意思
一張圖代表AI達成任務的難易度里程碑

人工智能的發展史:
1958年，有了兩個流派的發展路線，第一個 The Neats，由John McCarthy等人提出，強調的是不需要讓計算機與人類有著同樣的思考方式，需要的就是規則，邏輯，專家系統；另一方面，由Marvin Minsky等人提出的則是更接近人的思維框架，The Scruffies。當時由於計算力的不足，The Neats並沒有如同現在般占優勢。大約在1980年代之後，由於算力的精進，與之相關的神經網絡再次引起了注意。
在1988年以後引入了更多的其他學科的概念，包含概率論和決策理論，如貝葉斯網絡，隱馬爾可夫模型，信息論，隨機模型和經典優化理論等等。
直到1997年，IBM的深藍電腦與前蘇聯Gary Kasparov下國際象棋的獲勝成為一個標誌性里程碑，而其算力為最初Ferranti Mk1的一千萬倍。
2010年由於移動網絡，移動計算機的出現，一下子許多人都有了可供隨時使用的計算機，尤其是智能手機帶來的巨大影響。因此，幾乎是一瞬間網絡上的數據出現了近一步爆炸性的增長。


## 神經網絡的架構
input layer
The Hidden layer
Output layer

人類在其中的角色: 幫助參數的調節

Deep learning 可區分成兩階段，第一是Training/ learning，應用訓練集 (traning data set)找到最好的 weight 與 bias，第二是 Application，則是運用已經調整好訓練好的AI。

#### Training 的手法
Supervised Learning: training set is labeled (模擬題有標準答案)
Unsupervised Learning: training set is not labeled (模擬題沒有標準答案，但是我把訓練集做一些分析推測，接著反過來做修正參數)
Reinforcement Learning: training is a sequence of trial and reaction (trial and feedback，有點聽不懂)

與標準答案的差距，稱為**the losses**。接著回過頭讓機器調整據此調整參數。
反向傳播: 怎麼通過 losses 去反過來優化算法，幫助神經網絡更快找到高效的穩定網絡算法。

## 當前主流機器學習框架: TensorFlow 與 Pytorch
### TensorFlow

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

