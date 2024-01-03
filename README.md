# ○ Subject: 음성인식 및 텍스트 분석을 활용한 비대면 진료

# ○ Contributer

팀원|역할|
------------|-----------------------
김가은(팀장) | 서비스 기획, 데이터 크롤링 
　　　　　　　| 텍스트 기반 예측 모델 구축, PPT 제작   
김동신(팀원) | 서비스 기획, 데이터 전처리         
　　　　　　　|  ASR 모델 구축, 음성 데이터셋 분류              
한동(팀원) | 서비스 기획, 회의록 작성
　　　　　　　| ASR 모델 구축, 음성 데이터셋 분류
---
### ○ Skils: STT , Whisper(API) , TF-IDF , Keras, librosa , ( waveform,spectogram ; 시각화 )

### ○ Model: CNN, ASR

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
