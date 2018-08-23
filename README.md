
# PMS7003 프로토콜 예제 코드

**라즈베리파이**에서 사용되는 **PMS7003/PMS7003M**의 **Python**예제 코드입니다.  

엘레파츠에서 두 먼지센서는 아래 링크에서 만나보실 수 있습니다.  
PMS7003 : https://www.eleparts.co.kr/EPXHUUNM  
PMS7003M : https://www.eleparts.co.kr/EPXHWJ6L  


## menual  

사용자  매뉴얼 입니다.  

- 제품 구성 및 조립 방법 등이 자세히 설명되어 있습니다.  
-준비 중

## PMS7003.py

예제 코드 파일입니다.
직접 실행하는 경우 Serial설정을 환경에 맞게 수정해 주어야 합니다.

``if  __name__=='__main__':  `` 내부의  
``serial.Serial(UART, Speed, timeout  =  1) ``  
UART 부분을 PMS7003의 연결방법에 맞게 수정한 뒤  
``sudo puthon3 PMS7003.py``  
위 명령어로 실행해 주시면 Terminal창에서 데이터를 받아볼 수 있습니다.  
기본값 : UART = '/dev/ttyAMA0'  


## dust_chk.py

위 PMS7003.py 파일을 import 하여 실행하는 예제입니다.  

실행 전 코드의 **시리얼 설정** 부분(하단 코드 참고)을 연결 방식에 맞춰 수정해준 뒤   
```
# UART / USB Serial
USB =  '/dev/ttyUSB0' #USB 사용시  
UART =  '/dev/ttyAMA0' # UART 사용시  

#serial setting  
ser = serial.Serial(UART, Speed, timeout  =  1)  
```
``sudo puthon3 dust_chk.py``   
위 명령어로 실행해 주시면 됩니다.


## data sheet 
PMS7003및 PMS7003M의 데이터시트(영문)이 저장되어 있습니다.

