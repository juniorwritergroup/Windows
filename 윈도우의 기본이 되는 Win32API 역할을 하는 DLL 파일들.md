# 윈도우의 기본이 되는 Win32API 역할을 하는 DLL 파일들

DLL : 작은 프로그램들의 집합으로서 컴퓨터 내에서 실행되고 있는 큰 프로그램에서 필요로 할 때 그 중 어떤 것이라도 호출 될 수 있다. 

### 1. Kernel32 DLL

하드웨어가 사용하는 메모리와 사용자가 메모리로 윈도우의 메모리 운영이 나누어져있습니다.



위의 그림은 Kernel mode 단에서 각종 프로토콜, 그리고 하드웨어 드라이버들이 있고 그 위의 user mode라고 해서 실제로 사용자가 프로그램을 실행하는 윈도우가 되는데....

아래 kernel mode에서 user mode로 넘어오는 하단의 Ntdll.dll이 있는데

이 Ntdll.dll 파일은 윈도우가 부팅되면서 커널 메모리 영역을 사용할 수 있게끔 해주는 중요한 역할을 합니다.

Ntdll.dll 파일과 kernel32.dll 파일은 한 몸이라고 볼 수 있습니다.

##### 부팅시 로드되어 모든 프로그램에 사용되며, 커널이 어플리케이션에게 제공할 수 있는 서비스들이 함수 형태로 들어있다. 프로세스와 스레드, 메모리 관리를 합니다.

(ntdll.dll : kernel32.dll과 함께 부팅시 로드되어 모든 프로그램에서 사용되며 커널 메모리 영역을 사용할 수 있도록 해주는 역할을 한다.)



### 2. User32.dll

유저 인터페이스와 관계된 API함수들을 포함하고 있는 dll. 윈도우 어플리케이션에서 창을 띄우고 관리하는 모든 기능을 포함하고 있습니다.



### 3. GDI32.dll

윈도우에서 마우스, 그림, 화면 등 사용자의 GUI의 가장 기본이 되는 dll