# 회고<br>
## 어려웠던점<br>
- LSTM학습 시간이 많이 걸려서 다시한번 computing power가 좋아야 함을 알게되었습니다.<br>
- get_hidden_size, get_embedding_size 함수로 처리하면 너무 많은 시간이 걸려서 hidden_size를<br>
- 적당한 값으로 고정해서 간신히 85%를 달성할 수 있었습니다.
## 알아낸점<br>
## 아직모호한점<br>
- 학습 및 테스트 데이터 만들때 \<BOS\>를 삽입했으나 문장전체를 보고 <br>
  긍정과 부정을 판별하므로 \<BOS\>를 삽입하지 않아도 될것 같다는 생각을 하게되었습니다<br>
- LSTM학습중 4 epoch 를 넘어가면 val_loss 값이 증가하는 이유가 모호합니다<br>
- LSTM hidden layer, embedding size 를 선택하는 기준에 대한 이유를 모르겠습니다<br>
## 자기다짐<br>