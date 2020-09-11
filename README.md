# git-forlk
git fork 협업방식 정리

## TODO
1. Eclipse에서 git clone 진행하기
2. git remote upstream 설정하기 - 세 명이 공유하는 저장소(upstream)

### 1. Eclipse에서 git clone 진행하기
<img src="" width="500" height="500"/>
 
#### 먼저 Windows -> Show View -> Other 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92923749-e1cd5200-f472-11ea-97db-a413850fe23d.png" width="500" height="500"/>



#### Git에서 Git Repository 를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92923886-26f18400-f473-11ea-99c3-a8c3aa08316d.png" width="500" height="500"/>



#### Git Repository 목록 중에서 중간에 git clone 으로 적혀 있는것을 눌러줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92924159-72a42d80-f473-11ea-9b38-788bd608b086.png" width="500" height="500"/>


#### 현재 자신이 Eclipse에 git clone 할 주소를 다음과 같이 복사를 해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92924370-cdd62000-f473-11ea-885c-e865b8620c1c.png" width="500" height="500"/>



#### Eclipse에서 git clone을 눌러주면 다음과 같이 뜨기에 github 페이지에서 복사한 주소를 URL에 복사해주고, User, Password도 입력해주고 Next를 누릅니다.
![image](https://user-images.githubusercontent.com/45028904/92925363-5dc89980-f475-11ea-9ed4-a62cae30de48.png)

#### Next를 누르면 다음과 같은 branch들이 나옵니다. 기존에 존재하는 브랜치들이기에 모두 선택하고 Next를 눌러줍니다.
![image](https://user-images.githubusercontent.com/45028904/92925453-79cc3b00-f475-11ea-835d-8eab06454b52.png)

#### git Repository를 어디에 Clone을 할지 경로를 정해줍니다.
![image](https://user-images.githubusercontent.com/45028904/92925604-b39d4180-f475-11ea-8193-ea8bba394fe9.png)

#### finish를 클릭하고 나면 Git Repository에 devst 또는 자신의 레포지토리가 있는 것을 확인할 수 있습니다.
![image](https://user-images.githubusercontent.com/45028904/92925775-f52dec80-f475-11ea-9bc0-96e0a5e9f21d.png)

### 2.git remote upstream 설정하기 - 세 명이 공유하는 저장소(upstream)
* Fork한 레포지토리에서 upstream인 레포지토리에 원격으로 연결하기 위해서 하는 작업이다.

#### Create Remote를 클릭해줍니다.
![image](https://user-images.githubusercontent.com/45028904/92925939-40e09600-f476-11ea-8754-0593ff1f135f.png)

#### Remote name으로 upstream으로 입력을 해주고 일단 Configure push 기본값으로 설정하고 Create를 해줍니다.
![image](https://user-images.githubusercontent.com/45028904/92926190-a0d73c80-f476-11ea-869b-fde4762afec5.png)

#### 기존에 origin으로 Fork한 저장소가 존재하기에 Change를 눌러줍니다.
![image](https://user-images.githubusercontent.com/45028904/92926409-f14e9a00-f476-11ea-93e2-acbbd9e6bc71.png)

#### 아까와 비슷한 화면이 뜨는데 이번에는 upstream인 dcu-devst/devst 저장소의 경로를 github에 들어가서 붙여넣기 해줍니다. 그리고 Finish를 누릅니다.
![image](https://user-images.githubusercontent.com/45028904/92926566-2ce96400-f477-11ea-9746-fefa3ca020bf.png)

#### 그러고 나면 다시 앞의 화면이 나오면 일단은 Save를 해줍니다.
![image](https://user-images.githubusercontent.com/45028904/92926637-4c808c80-f477-11ea-9d33-d44542e0112e.png)

#### 앞의 설정을 하고 나면 이와같이 upstream이 추가된 것을 볼 수 있습니다.
![image](https://user-images.githubusercontent.com/45028904/92926684-5efac600-f477-11ea-86c9-499e35ac7824.png)

#### 하지만, 여기서 하나 더 추가해줘야 합니다. 










