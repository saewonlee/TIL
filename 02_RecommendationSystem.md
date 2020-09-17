# 추천시스템

### 추천시스템이란?

------------

> 사용자가 좋아하고 관심을 가질만한 콘텐츠 혹은 상품을 데이터 기반으로 분석하여 추천해주는 시스템. 이를 통해 잠재 욕망, 소비를 이끌어 냄으로 이익의 극대화 할 수 있다. 넷플릭스, 왓챠, 아마존 등 다양한 산업군에서 추천시스템 알고리즘을 사용하고 실제로 효과를 보고 있다.



### 문제 정의

> ***정보과잉의 시대***

- 정보 기술의 발달로 정보 생산성이 급성장 하고있으며 이러한 현상 속에서 소비자는 자신이 원하는 정보를 찾는데 종종 어려움을 겪고 정보의 정확도 또한 떨어진다.
- SNS 사용자 10명 중 3명이 SNS 피로증후군을 경험했다고 답했고, 불특정 다수에게 자신의 사생활이 노출되는 것이 싫다 (34.1%)거나 흥미와 관심이 떨어졌다 (43.9%)는 이들도 많았다. (한국일보, 2017)
- 기업의 입장에선 정보과잉의 시대에 얼마만큼 정확하고 알맞는 정보를 취할 수 있는지가 관건 (조선비즈, 2013)



### 추천시스템의 종류

#### (1) 협업 필터링 모델 (Collaborative Filtering)

> 기존 사용자들의 행동 정보 빅데이터를 분석하여 해당 사용자와 비슷한 성향의 사용자들이 기존에 좋아했던 항목을 추천하는 기술이다.

- 예를 들어, 사용자 A와 사용자 B가 사과와 오렌지를 같이 구매 했으므로, 사과를 구매한 사용자 C에게 오렌지를 추천한다. 

![img](https://lh5.googleusercontent.com/ojguJ85rfPmIrDABMw9QC7CBgBRWrIcK4qy1wNfZaXlxyjcPfTYGnscPQHhc3RA5kjaZlMTdn7zFSmjWOX44VSzxwT36Ae9YczmH4cK0WZXA-s36eYOQS4D_MFFSyQDnj2lXVBM)



#### *협업 필터링의 단점*

1. **콜드 스타트 (Cold Start)**

> 다중 사용자들이 기존 아이템에 대해 평가한 선호도를 기반으로 다음 아이템을 추천하는 모델인데, 만약 새로운 아이템이 추가 되었을 때 이 아이템이 사용자들로부터 평가를 받기까지 즉, 다음 추천을 위한 충분한 데이터가 쌓일 때까지 오랜 시간이 필요하다.



2. **롱테일 (Long Tail)**

> 선택지가 많다 해도 사용자들은 소수 인기 항목들에 편향되는 경향이 있다. 그래서 데이터는 점점 더 양극화 되고 결국 비교적 좋은 아이템이 있어도 추천을 할 수 있는 기반 데이터가 적어 문제를 야기한다.





#### (2) 콘텐츠 기반 필터링 모델 (Content-based Filtering)

> 협업 필터링이 사용자의 행동 데이터를 이용하는 반면, 콘텐츠 기반 필터링은 아이템 자체를 분석하여 추천을 구현한다. 예를 들어, 음악을 추천하기 위해 음악 자체를 분석하여 (음악 장르, 가수, 나라, 길이 등) 유사한 음악을 추천하는 방식이다. (아래 그림 오른쪽 참고)

![추천시스템(Recommender System)](https://lh3.googleusercontent.com/TyWfgZl0sNNWTKa60fsSXm4wlJhL5twc-eoQQ7uiAaANWIUvQII2y-pBIbiR_3QnCDm8a4RAgVU086UBOSLej0iFqsxakB7gojJ3jZ2VY_SklRJm_SikP48q-DBZ83EyqkP-5Zo)



#### *콘텐츠 기반 필터링의 단점*

1. **다양한 형식 추천 어려움**

> 콘텐츠 기반 필터링 모델 특성상 콘텐츠들을 분석하고 각 특징들을 카테고리화시켜 데이터로 저장하고 이를 추천에 사용한다. 하지만 다양한 형식의 아이템이 추가되면 상이한 형식의 아이템들의 특징을 통일시키기 어렵다.
>
> 예를 들어, 비디오와 사진은 다른 아이템 형식으로 서로 다른 특징들을 가지고 있고 얻을 수 있는 정보가 달라 프로파일 구성이 어렵다. 



2. **낮은 정확도**

> 협업 필터링 모델과 비교했을 때 대체로 더 낮은 정확도를 보이는 것으로 나타났다.



#### (3) Hybrid 추천 모델 (Hybrid Recommender System)

> 위 두 모델의 단점들을 해결하기 위해 고안된 모델로, 사용자 평점 기반 데이터에  콘텐츠 기반 데이터의 가중치를 주고 두개를 합산하여 좀 더 정확한 결과물을 낼 수 있는 모델이다.
>
> 콜드 스타트를 방지하기 위해 신규 아이템에 대해서는 콘텐츠 기반 데이터의 가중치가 보완재 역할을 하고, 반대로 콘텐츠 기반 필터링의 단점은 협업 필터링 모델로 상쇄하는 상호보완적인 알고리즘 모델이다.

![추천 시스템(Recommendation system)이란? - content based filtering, collaborative  filtering](https://lh5.googleusercontent.com/WEmMRHr2eWRCAh9k6GevL3FrSNBKkIxwgQt8R6-KnCj7ivZJifbeonSaoF7UjYTzIvAXqHh9kHuJiIeeu92s8gFghsDPdHEVDBKCnZAmEraGLAMijeWKcoEEYXqDNXaWQzBjsWs)

​    



