# git-fork
git fork 협업방식 정리

## TODO
1. Eclipse에서 git clone 진행하기
2. git remote upstream 설정하기 - 세 명이 공유하는 저장소(upstream)
3. Git Repository에 있는 devst를 Eclipse의 프로젝트로 생성하기
4. 변경사항을 관리하도록 branch를 생성해서 작업을 해보고 저장소에 올리기


### 1. Eclipse에서 git clone 진행하기
 
#### 먼저 Windows -> Show View -> Other 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92923749-e1cd5200-f472-11ea-97db-a413850fe23d.png" width="1000" height="700"/>

#### Git에서 Git Repository 를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92923886-26f18400-f473-11ea-99c3-a8c3aa08316d.png" width="1000" height="700"/>

#### Git Repository 목록 중에서 중간에 git clone 으로 적혀 있는것을 눌러줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92924159-72a42d80-f473-11ea-9b38-788bd608b086.png" width="1000" height="700"/>

#### 현재 자신이 Eclipse에 git clone 할 주소를 다음과 같이 복사를 해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92924370-cdd62000-f473-11ea-885c-e865b8620c1c.png" width="1000" height="700"/>

#### Eclipse에서 git clone을 눌러주면 다음과 같이 뜨기에 github 페이지에서 복사한 주소를 URL에 복사해주고, User, Password도 입력해주고 Next를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92925363-5dc89980-f475-11ea-9ed4-a62cae30de48.png" width="1000" height="700"/>

#### Next를 누르면 다음과 같은 branch들이 나옵니다. 기존에 존재하는 브랜치들이기에 모두 선택하고 Next를 눌러줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92925453-79cc3b00-f475-11ea-835d-8eab06454b52.png" width="1000" height="700"/>

#### git Repository를 어디에 Clone을 할지 경로를 정해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92925604-b39d4180-f475-11ea-8193-ea8bba394fe9.png" width="1000" height="700"/>

#### finish를 클릭하고 나면 Git Repository에 devst 또는 자신의 레포지토리가 있는 것을 확인할 수 있습니다.
<img src="https://user-images.githubusercontent.com/45028904/92925775-f52dec80-f475-11ea-9bc0-96e0a5e9f21d.png" width="1000" height="700"/>

### 2.git remote upstream 설정하기 - 세 명이 공유하는 저장소(upstream)
* Fork한 레포지토리에서 upstream인 레포지토리에 원격으로 연결하기 위해서 하는 작업이다.

#### Create Remote를 클릭해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92925939-40e09600-f476-11ea-8754-0593ff1f135f.png" width="1000" height="700"/>

#### Remote name으로 upstream으로 입력을 해주고 일단 Configure push 기본값으로 설정하고 Create를 해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92926190-a0d73c80-f476-11ea-869b-fde4762afec5.png" width="1000" height="700"/>

#### 기존에 origin으로 Fork한 저장소가 존재하기에 Change를 눌러줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92926409-f14e9a00-f476-11ea-93e2-acbbd9e6bc71.png" width="1000" height="700"/>

#### 아까와 비슷한 화면이 뜨는데 이번에는 upstream인 dcu-devst/devst 저장소의 경로를 github에 들어가서 붙여넣기 해줍니다. 그리고 Finish를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92926566-2ce96400-f477-11ea-9746-fefa3ca020bf.png" width="1000" height="700"/>

#### 그러고 나면 다시 앞의 화면이 나오면 일단은 Save를 해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92926637-4c808c80-f477-11ea-9d33-d44542e0112e.png" width="1000" height="700"/>

#### 앞의 설정을 하고 나면 이와같이 upstream이 추가된 것을 볼 수 있습니다.
<img src="https://user-images.githubusercontent.com/45028904/92926684-5efac600-f477-11ea-86c9-499e35ac7824.png" width="1000" height="700"/>

#### 하지만, 여기서 하나 더 추가해줘야 합니다. 위의 설정은 아직 upstream의 경로만 추가가 해준것이기에 fetch가 가능한 upstream 저장소의 origin을 등록해줘야 합니다. 여기서 origin이란 일단은 master라고 생각하면 될거 같습니다.
<img src="https://user-images.githubusercontent.com/45028904/92926872-a84b1580-f477-11ea-8c93-4a220302cacf.png" width="1000" height="700"/>

#### 환경설정 파일을 Open을 눌러서 열어서 설정해주겠습니다.
<img src="https://user-images.githubusercontent.com/45028904/92927035-f19b6500-f477-11ea-8888-c8a00d8b7dbe.png" width="1000" height="700"/>

#### config 관련 설정 파일이 나옵니다. remote "origin"에 현재 제가 Fork한 저장소의 url과 fetch 경로가 나옵니다. 그래서 위 fetch를 하단의 remote "upstream"에서도 추가해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92927340-6bcbe980-f478-11ea-91fb-1f02697684f9.png" width="1000" height="700"/>

#### remote "upstream"에 fetch를 추가해주고 ctrl + s 로 꼭 저장해줍니다. 이로써 git remote 연결은 완료했습니다.
<img src="https://user-images.githubusercontent.com/45028904/92927402-83a36d80-f478-11ea-8701-806a0334c9b3.png" width="1000" height="700"/>

### 3. Git Repository에 있는 devst를 Eclipse의 프로젝트로 생성을 하겠습니다.

#### Project Explore에서 우측 마우스를 누른 뒤 다음과 같이 Import를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92927611-e09f2380-f478-11ea-942a-51bd5db9f441.png" width="1000" height="700"/>

#### Git 폴더에 Projects from Git을 선택하고 Next를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92927731-0b897780-f479-11ea-9338-5af259ae0fd3.png" width="1000" height="700"/>

#### 현재 저희는 아까 git clone 한 저장소에 upstream 설정을 해줘서 존재하는 저장소를 클릭합니다.
<img src="https://user-images.githubusercontent.com/45028904/92927885-468bab00-f479-11ea-8426-d5e011d61ea1.png" width="1000" height="700"/>

#### Next를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92927918-51ded680-f479-11ea-9698-b6ef1f1efeeb.png" width="1000" height="700"/>

#### 프로젝트 생성을 다음과 같이 누르고 Finish를 진행합니다.
<img src="https://user-images.githubusercontent.com/45028904/92928190-b863f480-f479-11ea-80a9-713480f9f582.png" width="1000" height="700"/>

#### 프로젝트 Import를 Finish 합니다.
<img src="https://user-images.githubusercontent.com/45028904/92928274-cfa2e200-f479-11ea-905c-bcd3c741d6ab.png" width="1000" height="700"/>

#### 생성을 하고 다음과 같이 project가 나오는 것을 볼 수 있습니다. 그렇지만 일반 프로젝트로 일단 Import를 했기에 Maven Project로 바꿔주면 pom.xml에서 자동으로 라이브러리를 설치해줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92928422-024cda80-f47a-11ea-99c1-21567014b882.png" width="1000" height="700"/>

#### 다음과 같이 Maven Project로 변경을 해줍니다. 변경이 되고나면 자동으로 pom.xml을 읽어 들이고 나서 Spring Project로 바뀌게 됩니다.
<img src="https://user-images.githubusercontent.com/45028904/92928559-3aecb400-f47a-11ea-8376-5fd94a48d67d.png" width="1000" height="700"/>

### 4. 변경사항을 관리하도록 branch를 생성해서 작업을 해보고 저장소에 올려보겠습니다.

#### devst 프로젝트 우클릭 후 -> Team -> Switch To -> New Branch 를 클릭합니다.
<img src="https://user-images.githubusercontent.com/45028904/92928769-8acb7b00-f47a-11ea-877e-3b1a1df41fa0.png" width="1000" height="700"/>

#### 현재 좌측에 devst 프로젝트에서는 devst master라고 브랜치가 있는것을 확인이 가능합니다. 새로운 브랜치는 임의적으로 일단 feautre/boardList라고 이름을 짓고, Finish를 눌러줍니다.
<img src="https://user-images.githubusercontent.com/45028904/92929163-1513df00-f47b-11ea-9a99-545d7c9e13c8.png" width="1000" height="700"/>

#### 생성을 하고 나면 위의 Check out new Branch로 설정을 했기에 바로 새로운 브랜치인 feature/boardList로 바꿔집니다.
<img src="https://user-images.githubusercontent.com/45028904/92929310-48ef0480-f47b-11ea-8d84-14aaec1c03f9.png" width="1000" height="700"/>

#### text.jsp를 하나 만들어서 변경 사항을 관리해보겠습니다. 간단하게 h2태그에 test 내용만 적습니다.
<img src="https://user-images.githubusercontent.com/45028904/92929484-93708100-f47b-11ea-84d5-a71323895881.png" width="1000" height="700"/>

#### 변경사항을 관리하기 위해서 Project 우클릭 후 -> Team -> Add to Index를 해줍니다. 그 전에 project에서 text.jsp가 어떤 모습으로 보이는지 확ㅇ니하고 Add to Index를 누르도록 하겠습니다.
 * 자세하게 보시면 다른 파일들은 노란색 점으로 되어 있는게 보일겁니다. 노란색으로 보이면 이미 git에 올라가있는 최신 변동사항인것이고, text.jsp 처럼 ?가 되어 있으면 아직 git에서 변동사항을 체크하지 못한것을 의미합니다. 그래서 Add to Index를 해주는 것입니다.

<img src="https://user-images.githubusercontent.com/45028904/92929775-0f6ac900-f47c-11ea-9c8e-168a99098e84.png" width="1000" height="700"/>


<img src="https://user-images.githubusercontent.com/45028904/92929657-df232a80-f47b-11ea-9e14-92c4d76773cf.png" width="1000" height="700"/>

#### 프로젝트에 *와 같은 문양이 떠있는것을 볼 수 있습니다. text.jsp에서는 +가 생겼고 변동사항을 체크했고 변동이 존재해서 프로젝트에서는 *가 생기는 것입니다.
<img src="https://user-images.githubusercontent.com/45028904/92930006-696b8e80-f47c-11ea-83df-757f821a2a1a.png" width="1000" height="700"/>

#### 이 다음은 변동사항을 체크했으니 이제는 commit 을 해야합니다. 
* 프로젝트 우클릭 후 -> Team -> Commit을 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92930100-95870f80-f47c-11ea-892e-7233df10b5aa.png" width="1000" height="700"/>

#### Commit을 누르면 Unstaged 영역과 Staged 영역이 나옵니다. 저희는 현재 text.jsp의 변동사항을 Add to Index를 통해서 했기에 Staged 영역에 볼 수 있습ㄴ디ㅏ.
* 그래서! 우측에 Commmit Message를 입력하고 하단에 Commit and Push를 바로 진행하도록 하겠습니다.
 * commit을 하면 저희가 지금 작업하고 있는 local pc에서 변동사항을 저장하는 것입니다.
 * push의 경우에는 local pc => 저희가 Fork한 pc 업로드 하는 것입니다.
  * 여기서는 upstream로 또한 저희가 공유하는 저장소를 remote로 연결을 해서 github 페이지에서 올라온 변동사항을 확인이 가능합니다.
 
 <img src="https://user-images.githubusercontent.com/45028904/92930578-383f8e00-f47d-11ea-9b0a-d231b241bf71.png" width="1000" height="700"/>

#### 누르고 나면 이제 어떤 브랜치로 push를 하는지 물어봅니다. 당연히 저희는 feature/boardList 브랜치로 선택하고 Next를 누릅니다.
<img src="https://user-images.githubusercontent.com/45028904/92930698-61f8b500-f47d-11ea-9663-92e3d5662552.png" width="1000" height="700"/>

#### Next를 누르고 나면 조금의 시간 뒤에 Push Confirmation 화면을 볼 수 있습니다.
<img src="https://user-images.githubusercontent.com/45028904/92930783-7e94ed00-f47d-11ea-97b5-e7f5cd4664f8.png" width="1000" height="700"/>

#### 자신이 Fork한 github 페이지의 개인 저장소에 들어가면 다음과 같은 항목이 뜹니다.
 * 아래와 같은 내용은 feautre/boardList 브랜치로 작업이 성공적으로 올라갔고 항목을 누르면 pull requet 즉 저희가 공동 관리하는 upstream에 반영해달라고 작성을 하는 것입니다.

<img src="https://user-images.githubusercontent.com/45028904/92930961-bd2aa780-f47d-11ea-9078-dab34a49a9f4.png" width="1000" height="700"/>

#### compare & pull request 버튼을 누르면 저희가 공동 관리하는 dcu-devst/devst 저장소로 와서 요청 내용을 입력하고 하단의 3번의 Creata pull Request를 눌러 요청합니다.
<img src="https://user-images.githubusercontent.com/45028904/92931310-3c1fe000-f47e-11ea-9d9c-1488a3c0b40a.png" width="1000" height="700"/>

#### 여기서는 이제 팀원이 3명이라면 규약을 정해놓고 만약 2명이 확인을 해서 하단에 댓글을 달면 마지막 사람이 Merge를 하는 방식으로 변경사항을 반영해야지 이제 feature/boardList 브랜치에서 작성한 결과가 반영이 되는 것입니다.
<img src="https://user-images.githubusercontent.com/45028904/92931680-c8ca9e00-f47e-11ea-9706-cf8ad9e5e3df.png" width="1000" height="700"/>

#### Merge를 진행하고 나면 Merged가 된 보라색 화면을 볼 수 있습니다.
<img src="https://user-images.githubusercontent.com/45028904/92932079-5dcd9700-f47f-11ea-95f0-0719bf66830a.png" width="1000" height="700"/>


### 5. Fork한 feature/boardList 브랜치와 upstream 인 세 명이서 공유하고 있는 저장소는 text.jsp가 업데이트 되었지만, Fork한 master 브랜치에서 upstream의 변동사항을 가져와야한다.

#### devst 프로젝트에서 현재 feaute/boardList 브랜치는 text.jsp를 가지고 있는것을 볼 수 있습니다. 그러면 master 브랜치로 변경하고 확인해보겠습니다. 
<img src="https://user-images.githubusercontent.com/45028904/92940248-d9ccdc80-f489-11ea-9e5c-8e267791f36b.png" width="1000" height="700"/>

#### 변경 방법은 비교적 간단합니다.
  * 프로젝트 우클릭 후 -> Team -> Switch to -> master 로 변경을 해줍니다.
  
<img src="https://user-images.githubusercontent.com/45028904/92940460-1dbfe180-f48a-11ea-9325-146ccf6cd1f9.png" width="1000" height="700"/>

#### 변경을 하고나면 devst 프로젝트명 옆에는 master 브랜치가 선택이 된 것을 확인할 수 있고, 하단의 빨간 박스에는 어디에도 text.jsp는 없는 것을 볼 수 있습니다. 
  * 왜냐하면, 각각의 브랜치는 다른 공간이라고 생각하시면 됩니다. 그래서 Fork 한 저장소에서 feature/boardList 브랜치에서 text.jsp 작업을 하고, upstream 인 공동 저장소에 변동 사항을 반영해서 Fork의 master 브랜치에서 upstream의 최신 변동 사항을 가져와야 합니다.
 
<img src="https://user-images.githubusercontent.com/45028904/92940694-5fe92300-f48a-11ea-80eb-8c9f0b421ddc.png" width="1000" height="700"/>

#### 이제 upstream에서 pull 을 해와서 Fork 저장소의 master 브랜치에 최신 변동사항을 업데이트 해보기 위해서 pull이 두 개가 있는데 하단에 것을 클릭합니다.
<img src="https://user-images.githubusercontent.com/45028904/92941080-e0a81f00-f48a-11ea-829b-8c61e8827e03.png" width="1000" height="700"/>

#### 클릭을 하고나면 origin, upstream 선택을 하는 것이 있는데 저희는 upstream이 공용 저장소이니 upstream을 선택합니다.
<img src="https://user-images.githubusercontent.com/45028904/92941119-edc50e00-f48a-11ea-9f25-f1751302dd4b.png" width="1000" height="700"/>

#### upstream에서 최신 변동사항들을 잘 가져온것을 볼 수 있습니다.
<img src="https://user-images.githubusercontent.com/45028904/92941291-2664e780-f48b-11ea-9227-201e8cef5487.png" width="1000" height="700"/>

#### devst 프로젝트 우측에 master 브랜치인것을 볼 수 있고, upstream의 최신 코드가 정상적으로 반영이 되어서 하단의 text.jsp가 잘 있는것을 확인이 가능합니다.
<img src="https://user-images.githubusercontent.com/45028904/92941482-61671b00-f48b-11ea-9e02-c2e8beeed8a2.png" width="1000" height="700"/>



