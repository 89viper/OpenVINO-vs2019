# OpenVINO-vs2019

## OpenVINO 설치

OpenVINO 웹사이트 : https://software.intel.com/en-us/openvino-toolkit

## OpenVINO 설치 경로

C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033

## 샘플 돌려보기

OpenVINO 샘플 웹 사이트 : https://docs.openvinotoolkit.org/2020.1/_docs_IE_DG_Samples_Overview.html

## Inference Engine 샘플 및 데모 경로

샘플 : C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033\deployment_tools\inference_engine\samples<br/>
데모 : C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033\deployment_tools\inference_engine\demos

## Hello Classification C++ Sample 빌드하기

1. 새 프로젝트 생성(Empty C++)
2. main.cpp 복사
3. include 경로 설정
C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033\deployment_tools\inference_engine\include
C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033\inference_engine\samples\cpp\common
C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033\opencv\include

전처리기 설정에 _CRT_SECURE_NO_WARNINGS 추가
Unicode -> 멀티바이트로 바꾸기

4. 링크 경로 설정
C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033\deployment_tools\inference_engine\lib\intel64\Release
C:\Program Files (x86)\IntelSWTools\openvino_2020.1.033\opencv\lib

입력에
inference_engine.lib
opencv_core420.lib
opencv_imgcodecs420.lib
추가

5. dll파일들 복사해서 프로젝트 경로에 넣기
위에 추가한 lib에 해당하는 dll파일과
빌드 시 추가가 필요한 dll파일 추가
(이 프로젝트의 경우
ngraph.dll
opencv_improc420.dll
tbb.dll
을 복사해서 프로젝트 폴더에 붙여넣음)

6. 실행 콘솔창 확인

7. 코드 변경 후 실행
argv[1], argv[2], argv[3]이 모두 텍스트(경로)이므로
main.cpp 내에서 직접 변경하는 것으로 모델 실행 가능.




