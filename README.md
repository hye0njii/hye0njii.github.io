# hye0njii.github.io

운전자 졸음 감지

개인 프로젝트로 진행하였습니다.
Member : 장현지, 전기공학전공, guswl7598@hanyang.ac.kr

I. Proposal
- Motivation: Why are you doing this?
- What do you want to see at the end?
졸음운전은 혈중 알코올농도 0.17%의 만취 상태에서 운전하는 것rhk 같을 정도로 위험하다. 한국도로공사에 따르면 2016~2020 5년간 고속도로 교통사고 사망자 1035명 중 약 70%인 722명이 졸음 및 주시태만으로 인해 발생했다. 이러한 졸음운전을 방지하기 위한 연구들이 진행되고 있다. 이에 OpenCV를 이용하여 운전자가 졸 경우 이를 인식하는 모델을 운전자 dataset을 통해 테스트하고자 한다. 


II. Datasets

졸음운전 예방을 위한 운전자 상태 정보 영상 Dataset을 사용할 것이다.

![image](https://user-images.githubusercontent.com/105009129/171202884-d8a9065d-0cd2-4d46-b488-474f619c4ed7.png)

위의 dataset을 사용하고자 했으나, data 처리 과정에 어려움을 겪어 dataset을 변경했다.

https://github.com/kairess/eye_blink_detector/blob/master/README.md
위 github에서 dataset을 다운받아 사용했다.

III. Methodology 


![image](https://user-images.githubusercontent.com/105009129/174095824-6bcfb14a-035f-4bfa-b1b1-02998757dbbb.png)

Colab 환경에서 프로젝트를 진행했기에, Colab 환경 설정을 해주었다.

![image](https://user-images.githubusercontent.com/105009129/174096038-62320699-dd36-4741-a952-45a88f7bf3b9.png)

data를 불러오는 과정이다.
이 부분에서 내가 사용하고자 했던 졸음운전 예방을 위한 운전자 상태 정보 영상 Dataset을 이용하고자 했으나, 기존의 eyes_dataset을 사용했다.

![image](https://user-images.githubusercontent.com/105009129/174096461-ae01abd7-6f2b-4026-9710-805a06c21ede.png)

model을 만드는 과정이다. 

![image](https://user-images.githubusercontent.com/105009129/174096848-89d9dc3e-c3a7-4a26-b894-966469184df6.png)
input이 (26, 34)일 때의 모델 요약을 불러온 결과이다.


![image](https://user-images.githubusercontent.com/105009129/174097098-aabd78b5-6b8b-4377-a378-9f3c29bbdaad.png)

Colab에서 다른 파일을 import 하기 위해 필요한 import_ipynb를 설치했다.


![image](https://user-images.githubusercontent.com/105009129/174097473-102819ea-00d8-4f8e-8f7f-a0a732449bec.png)

train 하는 과정이다.

![image](https://user-images.githubusercontent.com/105009129/174097520-d7ecc19e-873e-464f-a153-473fae308a03.png)
2586
데이터의 라벨링이 잘 되었는지 확인하는 과정이다. 데이터의 총 개수가 2586개여서 len(train_dataset)-2580 으로 range를 조정하여 6개의 결과만 확인해 보았다.


![image](https://user-images.githubusercontent.com/105009129/174097881-5a9fea31-3ade-4a5c-8257-902a299451a9.png)


epoch을 10으로 설정했다.

![image](https://user-images.githubusercontent.com/105009129/174097996-c5475da7-c657-45f8-b4cc-35bba4b432ef.png)


결과는 다음과 같다


![image](https://user-images.githubusercontent.com/105009129/174098127-6ba2f870-9c5d-4445-aa58-41feea4964d1.png)


![image](https://user-images.githubusercontent.com/105009129/174098191-a0dbf11b-4932-4b4a-8a32-fc52d319cb6e.png)



![image](https://user-images.githubusercontent.com/105009129/174098231-b4ca783c-079e-49d4-aaea-dfafdac604cf.png)


![image](https://user-images.githubusercontent.com/105009129/174098302-fe2b97a2-5022-4cba-96e6-5c4485660287.png)


Test 코드는 다음과 같다.

![image](https://user-images.githubusercontent.com/105009129/174098675-02f7ccc2-74ab-4f3d-8662-b07da15ac7c3.png)


![image](https://user-images.githubusercontent.com/105009129/174098876-df83fa37-2512-459a-b5c2-5f11417c5475.png)

![image](https://user-images.githubusercontent.com/105009129/174098921-eadde198-708f-4e05-a9cc-d1453615fdcb.png)

![image](https://user-images.githubusercontent.com/105009129/174098974-18161b58-cfdd-408e-985e-a592453b51e9.png)


train loss를 최소화하기 위해 epoch의 수를 50으로 늘려서 다시 training을 했다.

![image](https://user-images.githubusercontent.com/105009129/174103298-1798a3d6-3b19-4085-9577-e300ade1fe44.png)


![image](https://user-images.githubusercontent.com/105009129/174103356-e17e4984-8ade-4507-80d9-86feabccef2c.png)


정확도가 낮아졌는데, 유의미한 변화는 아닌 것 같다.

IV. Related Work 
https://github.com/kairess/eye_blink_detector/blob/master/README.md
https://github.com/yunseokddi/Pytorch_dev/tree/master/sleep_detect

VI. Conclusion: Discussion
