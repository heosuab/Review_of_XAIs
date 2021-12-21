# Results

<br>

**※ 명확한 metrics가 존재하지 않으므로 모든 분석은 주관적인 생각입니다.**

<br>

#### [1. 모델의 성능에 따른 XAI 결과의 변화는?](https://github.com/heosuab/Review_of_XAIs/tree/main/review/base_dog)

>  **:mag_right: What's the ​idea?**
>
> ​	하나의 이미지에 대해서 CNN 모델들은 다른 prediction과 다른 확률을 보인다. 선정한 세 개의 모델이 "같은 예측"을 하더라도 **예측에 대한 확률이 다를 때, XAI 결과가 어떻게 다를지** 확인해보았다.

<br>

#### [2. Single object의 위치가 한쪽으로 치우친 경우에는?](https://github.com/heosuab/Review_of_XAIs/tree/main/review/side_cat)

>  **:mag_right: What's the ​idea?**
>
> ​	single classification CNN 모델들은 translation-invariance라는 특성을 가지고 있기 때문에, object가 이미지 상의 어떤 위치에 존재하든지 같은 prediction을 출력한다. 따라서 CNN모델의 output만으로는 object들의 위치를 알아낼 수 없지만, **모델 내에서 분석하는 XAI의 결과를 확인해보면 위치를 알아낼 수도 있지 않을까?** 라는 생각으로 확인해보았다. 

<br>

#### [3. 여러 class의 object가 있을 경우에는?](https://github.com/heosuab/Review_of_XAIs/tree/main/review/fruits)

> **:mag_right: What's the ​idea?**
>
> ​	학습된 여러 class의 여러가지 object가 하나의 이미지 안에 동시에 포함되어 있어도, Classification CNN 모델은 하나의 class만 최종 prediction으로 선정해야 한다. 이럴 경우에 모델 내부에서는 **어떤 object를 더 highlight하고, 최종 prediction과 heatmap의 연관성이 어떻게 나타날지** 궁금해져서 확인해보았다.

<br>

#### [4. 이미지 회전에 따른 XAI 결과 변화는?](https://github.com/heosuab/Review_of_XAIs/tree/main/review/rotate)

> **:mag_right: What's the ​idea?**
>
> ​	Image data augmentation이란, 학습 데이터로 주어진 데이터들에 여러 방법으로 변화를 주어 학습데이터의 양을 늘리고 정규화의 역할을 하는 데이터 증강 기법이다. 대표적으로 rotate, shift, flip 등의 방법이 있다. **실제로 augmentation이 CNN 학습에 도움을 줄 수 있는지** 살펴보기 위해 이미지를 의도적으로 180도 rotate시켜서 XAI 결과의 변화를 확인해보았다. 

<br>

#### [5. 학습되지 않은 object에 대한 결과는?](https://github.com/heosuab/Review_of_XAIs/tree/main/review/five)

> **:mag_right: What's the ​idea?**
>
> ​	학습되지 않은 object의 이미지가 들어오면 모델은 당연히 틀린 prediction을 만들 수밖에 없다. 하지만 결과의 정답 유무를 떠나서, **학습되지 않은 object에 대해서는 모델의 XAI 결과가 어떻게 나올지** 궁금해져서 확인해보았다.

<br>

#### [6. Object의 형태vs색깔?](https://github.com/heosuab/Review_of_XAIs/tree/main/review/apples)

> **:mag_right: What's the ​idea?**
>
> ​	지금까지 XAI 결과들을 확인해보니, XAI 기법은 object의 "위치" 또는 "형태"에 민감한 알고리즘이라는 생각이 들었다. 따라서 **object의 "색깔"이라는 feature에도 큰 중요도를 두는지** 궁금해져서, 색깔만 다른 object의 이미지를 어떻게 구분하는지 결과를 확인해보았다.

<br>

#### [7. Anomaly detection을 위한 XAI?](https://github.com/heosuab/Review_of_XAIs/tree/main/review/anomaly)

> **:mag_right: What's the ​idea?**
>
> ​	예전에 XAI 관련 논문을 서치해보다가, XAI를 통해 anomaly detection을 수행할 수도 있다는 연구를 보았던 기억이 있다. 앞서 "색깔"이라는 feature가 모델의 prediction의 중요한 요소였다는 결론에 접목해서, **색깔이 다른 object(anomaly)를 detection할 수 있을지** 실험해보았다.

