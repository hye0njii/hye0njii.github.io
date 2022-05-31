# hye0njii.github.io

운전자 졸음 감지


I. Proposal

졸음운전은 혈중 알코올농도 0.17%의 만취 상태에서 운전하는 것고 같을 정도로 위험하다. 한국도로공사에 따르면 2016~2020 5년간 고속도로 교통사고 사망자 1035명 중 약 70%인 722명이 졸음 및 주시태만으로 인해 발생했다. 이에 OpenCV를 이용하여 운전자가 졸 경우 이를 인식하는 모델을 구현해보고 데이터셋을 이용해 테스트하고자 한다. 


II. Datasets

졸음운전 예방을 위한 운전자 상태 정보 영상 Dataset을 사용할 것이다.
![image](https://user-images.githubusercontent.com/105009129/171202884-d8a9065d-0cd2-4d46-b488-474f619c4ed7.png)


III. Methodology

눈 깜박임에 대한 감지는 EAR(eye aspect ratio)를 이용하여 계산할 것이다.
![image](https://user-images.githubusercontent.com/105009129/171203160-29bde1bd-b6d1-4ac5-a15c-942cc109cd99.png)
눈을 감게되면 눈의 세로 비율이 작아져 EAR 비율이 작아진다. 이 값의 기준치를 설정하여 운전자가 눈을 감고있는 상황을 인지할 것이다.


IV. Evaluation & Analysis-Graphs, tables, any statistics (if any)
V. Related Work (e.g., existing studies)-Tools, libraries, blogs, or any documentation that you have used to do this project.
VI. Conclusion: Discussion
