# 입사담당자가 궁금해 할만한것 ㅣ 정확도가 낮아서, 이런것을 해봤다, 시행착오에 대한 설명 프로젝트를 통해서 무엇을 배웠느냐, 프로젝트 결과가 어떻게 됬든, 아카데미에서 어떤 것을 배우면서, 느꼈던 것을 말하고, '나'를 한장으로 표현할 수 있는것을 포트 폴리오로 링크로 노션이나 블로그들, 레쥬메파일을 만들어 놓고, 프로젝트에대해 간단히 적어놓고, 링크를 올리는 식으로 

# ○ Subject: 음성인식 및 텍스트 분석을 활용한 비대면 진료

# ○ Contributer

팀원|역할|
------------|-----------------------
김가은(팀장) | 서비스 기획, 데이터 크롤링 
　　　　　　　| 텍스트 기반 예측 모델 구축, PPT 제작   
김동신(팀원) | 서비스 기획, 데이터 전처리         
　　　　　　　|  ASR 모델 구축, 음성 데이터셋 분류              
한동훈(팀원) | 서비스 기획, 회의록 작성
　　　　　　　| ASR 모델 구축, 음성 데이터셋 분류
---
### ○ Skils: STT , Whisper(API) , TF-IDF , Keras, librosa , ( waveform,spectogram ; 시각화 )

### ○ Model: CNN, ASR

### ○ Dataset : https://competition.aihub.or.kr/hackathon/scheduleDetail/6

### ○ Project Schedule 23.9.12 ~ 23.10.6(약 3주)
***

- ## 기획

![image](https://github.com/KimDong-gue/Healthy_Care/assets/116249934/93e4a1b9-2e44-40f1-a873-c981e12d84fe)

- 섬이나 외곽지역에 사시는 분이나 의료취약계층, 여러가지 이유로 방문이 어려운 환자들을 타겟으로 삼았습니다.
- 음성 및 텍스트를 기반으로 환자의 증상을 진단하고, 더불어 생성형 API를 사용하며 증상에 맞는 건강식품 및 예방법, 운동등을 추천하는 서비스를 모토로 삼았습니다.
- 팬데믹을 기점으로, 전세계적으로 비대면 진료 관련 규제 완화되는 추세
- 환자의 편의성이 올라가고, 외진 지역의 의료공백이 줄어드는 효과가 있다.
- 비대면 진료 법제화 추진 주장 가속화 추세이다.
- 2023 한국어 AI 경진대회 출전
---

- ## Model evaluation

![image](https://github.com/KimDong-gue/Healthy_Care/assets/116249934/13635877-1151-4533-aadb-246d6c85ef72)
![image](https://github.com/KimDong-gue/Healthy_Care/assets/116249934/768d06ab-caec-46fa-8da5-214e71fb596f)
![image](https://github.com/KimDong-gue/Healthy_Care/assets/116249934/88736c0f-b145-4db8-b587-c3c00a74f1da)

---

- ## 시연영상

![image](https://github.com/KimDong-gue/Healthy_Care/assets/116249934/da75b67d-e432-4dce-9edf-cd2b024d8d32)

---

- ## Problem

- 텍스트 길이가 짧음: 증상을 판별하기에 음성 길이와 내용이 너무 짧음
- STT 정확도로 인한 내용 불일치: 불필요한 내용이 포함되어, TF-IDF 모델에 입력으로 제공되어 정확도가 떨어짐
- 다른 방식 탐색? 원하는 음성 데이터셋을 구축하기 위해서는 TTS 기술을 활용하여 텍스트를 음성으로 변환해야함
  - 증상 판별 보다는 << 환자 증상 입력을 위한 방식으로 활용 수정
