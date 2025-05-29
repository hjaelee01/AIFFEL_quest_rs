# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 이현재
- 리뷰어 : 조성호


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 학습 결과 eval_accuracy가 0.9를 넘는 코드가 제출되었다.
    - Bucketing을 사용하지 않은 Baseline 코드 결과는 팀원의 결과로 대체하였다.
![image](https://github.com/user-attachments/assets/df7b9f90-4dd3-4ecc-bd14-557b7eab4b60)

![image](https://github.com/user-attachments/assets/8aaa2f23-d278-43b4-8552-69573aa3f2f2)
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 데이터 분포를 시각화하는 내용에서 길이를 계산하는 과정과 데이터 길이를 눈금으로 표시하는 부분에 주석 처리가 잘 되어있다.
    - 자세히 적혀있긴 하지만 영어라서 이해하는 데 아주 편하지는 않았다.
![image](https://github.com/user-attachments/assets/45b121e8-4bb0-404c-9a9f-6efd6c16c940)

![image](https://github.com/user-attachments/assets/28952916-54a7-4f8c-9030-bf75e1674cab)
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 코드 상에 에러 디버깅이나 추가 실험은 찾아보기 힘들다.
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 회고 부분에서 베이스라인 모델과 Bucketing 수행 모델 간의 비교를 수행하고, 두 모델 간 차이점에 대해 설명하였다.
    - 변경한 하이퍼 파라미터가 2가지인데, 각각의 실험을 수행하지 못한 점을 아쉽다고 발표했다.
![image](https://github.com/user-attachments/assets/9dc37080-3ae1-46d5-8e78-90c465c92033)

        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 토크나이저 실행 함수와 metric 계산 함수를 선언하여 필요에 맞게 사용하였다.
![image](https://github.com/user-attachments/assets/63eb98fb-89b9-4195-a17a-e7d463b9321b)

![image](https://github.com/user-attachments/assets/6db6cd79-3e7d-4543-a964-911dec18d529)


# 회고(참고 링크 및 코드 개선)
```
코더와 리뷰어의 프로젝트 결과가 매우 유사하게 나온 점이 인상깊었다.
현재 님이 Bucketing을 통해 학습시간을 단축하실 때 fp16도 함께 적용하여 Bucketing과 fp16 중 어떤 방식의 효과로 학습 시간이 단축되었는지 확실치 않다고 말씀하셨지만, 제 프로젝트에서는 baseline에도 fp16을 적용하였고, Bucketing에서 시간 단축을 확인할 수 있으므로 bucketing이 시간 단축에 기여한다고 볼 수 있을 것 같습니다.
```
