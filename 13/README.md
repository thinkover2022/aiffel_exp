# 회고<br>
## 어려웠던점<br>
 - 원래부터 dataframe의 user_id, movie_id값이 숫자로 되어있어서 문자를 숫자로변경하는루틴<br>
   을 사용하지 않아도 되겠다고 생각하고 csr_matrix를 동작시켰더니 shape[0]크기를 index가 <br>
   넘어선다는 에러가 발생해서 중간에 연속적이지 않은 id값이 존재하는것으로 의심하고 이전<br>
   lms예제에 있었던 enumerate를 사용한 user_to_idx, movie_to_idx를 생성하고 각 셀을 생성한<br>
   값으로 변경시키는 루틴을 수행하면서 에러가 해결되었습니다<br>
## 알아낸점<br>
## 아직모호한점<br>
- AlernatingLeastSquares(use_gpu=True)한 후에 학습속도는 빠르게 진행되지만 matrix multiply<br>
  를 implict에서 cuda multiply가 지원되지 않는다는 에러가 발생해서 찾다가 포기했습니다<br>
## 자기다짐<br>
