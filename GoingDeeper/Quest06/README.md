# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 이현재
- 리뷰어 : 강희봉

# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    -  한글 코퍼스를 가공하여 BERT pretrain용 데이터셋을 생성
    -  구현한 BERT 모델의 학습이 안정적으로 진행됨을 확인 ( model save 오류로 인해 학습 커브는 없으나 로그 기록으로 확인 )
    -  약 4.5M 파라미터를 가지는 모델 제작과 학습이 진행되었으며 model save 오류로 인해 학습 커브는 없으나 lr rate 변화 그래프 포함   
![image](https://github.com/user-attachments/assets/0369200e-15ec-43f7-9bfe-d83b3a468231)
![image](https://github.com/user-attachments/assets/08836204-b315-435e-bcc8-8bc5414ea0b8)
![image](https://github.com/user-attachments/assets/e21d5efe-49a0-481c-b3ec-9b922a0e4681)
![image](https://github.com/user-attachments/assets/e4afeca8-c1e9-4c9c-85b3-edd2a67724ee)

- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 주어졌던 코드외에 핵심 부분은 Masked LM 과 NSP 테스트 부분으로 생각된다.
    - 각각 함수로 작성되었으며 필요한 정도의 주석은 포함되어있음 ( 코드 캡쳐는 생략, 결과 캡쳐 )   
![image](https://github.com/user-attachments/assets/f49349ff-7a23-4d2a-ac03-062586e42060)
![image](https://github.com/user-attachments/assets/71c1db70-17a3-41a4-a0ec-45a685e4c761)

- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 대량의 데이터셋을 직접로드했던 문제와 특수토큰 처리 관련 디버깅 기록   
![image](https://github.com/user-attachments/assets/2966350f-1bcf-4449-9944-4555724e982c)

- [x]  **4. 회고를 잘 작성했나요?**
    - 회고에 느낀점 배운점등을 작성하였습니다.   
![image](https://github.com/user-attachments/assets/61393c37-7cda-45ec-bda3-407e069722e3)
![image](https://github.com/user-attachments/assets/35d7d4f9-6d1d-4315-9168-c47687715257)

- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 주어진 코드외에 테스트 코드도 반복 부분을 함수화하여 효율적으로 작성하였습니다.   
![image](https://github.com/user-attachments/assets/99ef655e-1f35-4330-b24d-4f3716932194)
![image](https://github.com/user-attachments/assets/38bff32b-47c8-454e-b433-6c6f3c1b6116)

# 회고(참고 링크 및 코드 개선)

- vacab encode_ 와 piece_to_id 등 관련 실험하신 부분이 흥미로웠습니다. 신경쓰지않고 있었지만 제대로 알고있지 않으면 언젠간 실수할 내용인듯하여 덕분에 확인했습니다.
- 회고 작성과 결과 및 분석을 분리하면 좋을것 같습니다. 
- 에러 부분 관련 코멘트 : mode.save를 하면서 에러가 난 것으로 보입니다. 이미 찾아보셨을 수 있지만 저는 없던 문제라 찾아봤습니다. callback으로 weight만 저장시엔 문제가 없는데 model save 시엔 get config 함수를 override를 꼭 해줘야하나봅니다. 해당 부분은 저도 얻어갑니다.
- 개인 회고 : 조건을 착각해서 모델을 지나치게 크게 잡아 시간이 오래 걸렸는데 저보단 덜하지만 조건이었던 1M보다 큰 4.5M 파라미터가 적용된 모델을 구성해서 학습이 오래걸리면서 발생한 문제들이 있는듯합니다. 일단 루브릭을 만족하는 최소 조건으로 완성부터하고 추가 진행을 해야겠다고 생각했습니다. 물론 1M 기준을 제대로 못봐서 그런거라 조건을 좀 더 제대로 확인해야겠다는 생각도 했습니다.  
