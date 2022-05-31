# hye0njii.github.io

운전자 졸음 감지
Title:
Members: Name1, Department, EmailName2, Department, EmailName3, Department, Email ...
I. Proposal (Option 1or 2)–This should be filled by May.3-Motivation: Why are you doing this?-What do you want to see at the end?
II. Datasets–이부분부터는나중에하셔도됩니다.단SKT AI 펠로우쉽지원을고려하고계신분들은미리시작하시길바랍니다.-Describingyour dataset 
III. Methodology -Explaining your choice of algorithms (methods)-Explaining features (if any)
IV. Evaluation & Analysis-Graphs, tables, any statistics (if any)
V. Related Work (e.g., existing studies)-Tools, libraries, blogs, or any documentation that you have used to do this project.
VI. Conclusion: Discussion


수많은 사람들이 하루 종일 밤낮으로 고속도로를 이용한다. 택시 운전사, 트럭 운전사, 버스 운전사, 그리고 장거리 여행객들은 모두 수면 부족을 겪는다. 결과적으로 졸릴 때 운전하는 것은 매우 위험하다. 대부분의 사고는 운전자의 피곤으로 인해 발생한다. 따라서 이러한 충돌을 피하기 위해 Python, Keras 및 OpenCV를 사용하여 작업자가 피곤할 때 알려주는 모델을 만들 것이다.

이번 딥러닝 프로젝트는 사람의 눈이 잠시 감겼을 때 이를 모니터링하는 졸음 모니터링 센서를 만드는 것이 목적이다. 졸음이 인식되면 이 모델이 운전자에게 알린다.
이 파이썬 프로젝트에서 OpenCV를 사용하여 카메라에서 사진을 수집하고 딥러닝 모델에 넣어 사람의 눈이 떠져 있는지 감겨져 있는지 판단한다.
이 프로젝트에 사용된 데이터 세트에는 눈을 감고 뜬 사람의 이미지가 여러 개 있다. 각 이미지에 레이블이 지정된다. 7천 개 이상의 이미지를 포함하고 있다.
그런 다음 CNN으로 모델을 제작한다. 이럴 땐 Keras를 쓰자. 완료되면 총 128개의 노드가 완전히 연결된다.
이제 코드를 실행하고 정밀도를 확인한다. 필요한 경우 하이퍼 파라미터를 조정한다. PyGame을 사용하여 GUI를 작성한다.
OpenCV를 사용하여 비디오를 수신하거나 웹캠을 대신 사용할 수 있다. 스스로 테스트 해보자. 5초 동안 눈을 감으면 모델이 경고하는 것을 볼 수 있다.
