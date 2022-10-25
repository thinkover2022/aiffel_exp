# 회고<br>
## 어려웠던점<br>
- 왜 masking을 사용하지 않으면 동작하지 않는지 잘 모르겠습니다
- encoder_masking =Masking(mask_value=0.0)(enc_emb)
- masking을 사용하지 않는 경우에 1번 decoder.predict 수행하면 0~16까지에 대한 전체 문장의 0번째단어,1번째단어....16번째 단어별 확률값이 나오게 되는줄 알았으나 정상적으로 동작하지 않아서 어쩔수없이 인터넷의 힘으로 이전에 누군가가 작성해 놓은 코드를 보니 masking을 적용하였고 masking을 적용하니 정상적으로 예측이 되는 알수없는 상황이 발생하였습니다. 
## 알아낸점<br>
## 아직모호한점<br>
- masking을 사용하지 않는 경우에 decoder_model.predict([target_seq] + states_value)<br>
- 에서는 17x7454의 배열이 나오는데 masking을 사용하면 1x7454 배열이 나오는 이유를 잘 모르겠습니다.<br>
## 자기다짐<br>