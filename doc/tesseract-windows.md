


## 4.0

git clone https://github.com/tesseract-ocr/tesseract tesseract
Run

cd tesseract
cppan
mkdir build && cd build
cmake ..



 
>path
현재 환경변수 정보 보여줌.
 
>set path
path명령과 동일한 현재 환경변수 정보와 동일한 path 정보와
pathext라는 시스템 실행파일 확장자 변수가 같이 나온다.
 
>set path =%path%;추가하고자하는경로;
ex) >set path=%path%;c:\java\bin;
환경변수 추가(일시적)
 
>setx path "%PATH%;추가하고자하는경로"
ex) >setx path "%PATH%;c:\java\bin"
환경변수 추가(영구적)
 
%path%를 하는 이유는 현재 환경변수에 path 정보를 가져와서 
현재 환경변수에 새로운 환경변수를 추가해야하기 때문입니다.

echo 명령어를 사용하면 %%를 이용하여 모든 환경변수 내용을 알아낼수 있습니다.
ex) echo %os%


## 출처
- http://visu4l.tistory.com/391 [뭐라 씨부리 쌌노?]
- https://github.com/tesseract-ocr/tesseract/wiki/Compiling#windows

