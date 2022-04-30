# 2022security

2022년도 CICIDS 2017 DataSet을 이용한 이상 탐지 프로젝트 깃허브입니다.



# 보고서(Report)
보고서는 docs 디렉토리 내에 pdf 파일을 참조하시면 됩니다.



# 프로젝트 소스 파일 (Source File)
프로젝트에 사용된 소스 파일은 src 디렉토리 내에 ipynb 파일을 참조하시면 됩니다.



# 프로젝트 환경
프로젝트는 구글 코랩(Colab) 환경에서 PyTorch를 이용해서 진행되었습니다.



# 데이터 전처리 (Data PreProcessing)
CICIDS 2017 데이터 셋의 데이터들을 모델에 입력으로 주기 위해, 원-핫 인코딩(One-Hot Encoding)을 진행했습니다.
Label 값 중 "BENIGN"은 정상, 나머지 Lable들은 "비정상"으로 분류해서 모델에 입력으로 넣어주었습니다.



# 모델(Model)
모델은 AutoEncoder의 "정상" Label 값을 가지는 데이터 셋만 학습 데이터로 넣어주었고, 학습된 데이터 이외의 데이터는 복원 능력이 떨어진다는 점을
이용해서 이상탐지를 수행하였습니다.
