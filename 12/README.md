# 회고<br>
## 어려웠던점<br>
- summa.summarizer.summarize()함수에서 입력텍스트를 데이터 전처리 하기전 데이터를 넘겨주지 않는경우<br>
  정상적으로 요약된 정보가 출력되지 않아서 애를 먹었습니다 그래서 원래데이터는 text컬럼으로 남겨두고<br>
  전처리가 완료된 데이터를 text_new컬럼에 삽입하는 방식으로 처리해서 나중에 비교할때 사용하도록 했습니다.<br>
## 알아낸점<br>
- pandas.read_csv(encoding='utf-8')로 해도 정상적으로 처리하는 것을 확인했고 summa.summarizer.summarize() 함수는<br>
  전처리를 하지 않은 데이터를 파라미터로 넣어 주어야 정상적으로 요약정보를 생성한다는 것을 알게되었습니다<br>
## 아직모호한점<br>
- 특히나 urllib.request.urlretrieve를 통해 수신한 실제 파일은 utf-8 인데<br>
  왜 pandas.read_csv(encoding='iso-8859-1')로 로딩 했는지 이유를 잘 모르겠습니다.<br>
## 자기다짐<br>
- LSTM과 어텐션 구조에 대해서 좀더 세밀하게 공부해야 할것 같습니다.
