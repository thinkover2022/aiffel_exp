# 회고<br>
## 어려웠던점<br>
- 아래 수식을 찾지 못하고 embedding_size와 hidden layer를 5000번 늘렸을 경우 학습하는데 너무많은 시간을 소비해서 다시한번 컴퓨팅 파워의 절실함을 느꼈습니다<br>
## 알아낸점<br>
- embedding_size 를 많이 늘리면 연산량이 늘어나서 적당한 값을 찾아야 하는데 아래와 같은 방식으로 값을 찾아보았습니다.<br>
```
if num_categories <= 1000 :
    embedding_dimensions = min(500, num_categories/2) # 둘 중 최소값
else: # num_categories > 1000 일때
    embedding_dimensions = 75.6496 * np.log(num_categories + 176.623) - 41.4457
```
- LSTM hidden layer 개수<br>
$Nh = \frac{Ns}{(α∗(Ni+No))}$
```
Ni = 입력뉴런의 개수 (embedding_size)
No = 출력뉴런의 개수 (12000 )
Ns = 학습데이터 집합에서 샘플의 개수 (학습데이터개수 * embedding_size)
α = 임의의 스케일 요소 (일반적으로 2 사용)
```
## 아직모호한점<br>
- 어찌하여 위와같은 식이 나온것인지는 아직까지 이해하지 못하고 있습니다(구글의 힘을빌렸습니다)<br>
## 자기다짐<br>
- 논문에 제시된 내용을 이해하기위해 앞으로 더욱더 노력해야할것 같습니다<br>