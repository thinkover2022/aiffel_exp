# 회고<br>
## 어려웠던점<br>
- text원본데이터를 전처리 시킨 후에 생성된 데이터를 이용하여 summa.summarizer.summarize()함수에서<br>
  요약정보가 생성되기를 원했으나 정상적으로 요약 정보가 출력되지 않아서 애를 먹었습니다<br>
## 알아낸점<br>
- pandas.read_csv(encoding='utf-8')로 해도 정상적으로 동작하는 것을 확인했습니다<br>
- summa.summarizer.summarize() 함수는 전처리를 하지 않은 원본데이터를 파라미터로 넣어 주어야<br>
  정상적으로 요약정보를 생성한다는 것을 알게되었습니다<br>
## 아직모호한점<br>
- urllib.request.urlretrieve를 통해 로컬에 받은 실제 파일은 utf-8 로 인코딩 되어 있는데<br>
  왜 판다스에서 읽을때 pandas.read_csv(encoding='iso-8859-1')로 처리 했는지 궁금합니다<br>
## 자기다짐<br>
- LSTM과 어텐션 구조에 대해서 좀더 세밀하게 공부해야 할것 같습니다.
