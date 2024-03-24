# GitHub

<br>

## 작성자
- ### 해당 내용은 @linjuuu 님께서 작성해주셨습니다!
    - https://github.com/linjuuu

<br><br>

## 기초, 필수 내용

정말 기본적으로 쓰이는 내용들만 작성해보았습니다 ! 

이게 정석이 아닐 수 있으며, 쉽게 작성하다보니 실제와 다른 내용이 있을 수 있습니다 ! 

### git clone 저장소url

- 해당 깃허브 저장소에 저장된 파일들을 로컬저장소 (본인 컴퓨터) 에 저장할 수 있습니다.
- 예를 들어 디비전의 ‘레몬 크롤링 레포지토리’ 를 제 컴퓨터에 저장해볼게요
    
    <img width="828" alt="Untitled" src="https://github.com/Project-Division/about_react/assets/68108664/9e49742f-9579-4a06-8174-afd10c41c79a">
    
- 명령어를 실행한 폴더에 해당 깃허브 주소의 파일들을 다운로드 받은걸 확인할 수 있습니다.
- 처음에 프로젝트를 다운받을 때 사용하거나, 개발을 하다가 지금 있는 파일들 너무 꼬여서 되돌아가기 어렵다 싶을 때 그냥 지워버리고 clone 할 때 사용할 수 있습니다.

<aside>
💡 clone 하고 나서 어떤 코드를 작성하든, 아직 깃허브에는 반영되지 않으니 마음 편하게 작업하시면 됩니다.

</aside>

### 깃허브 업로드 - 작업물을 깃허브에 올릴 때 !

- git add .
    - 현재까지의 작업물을 add (업로드 목록에 추가 시키겠다)
    - . 은 모든 파일을 의미합니다.
    - 즉, git add . 은 지금까지 작업한 파일 모두 업로드할 목록에 추가 시키겠다는 의미입니다.
- git commit -m “메시지”
    - 이제 깃허브에 업로드를 할텐데, 지금 했던 작업이 무엇인지 기록하는 과정이 필요합니다.
    - git commit -m “gpu 크롤링 파일을 구현했습니다”   이런식으로 작성하면 됩니다.
    - 이제 업로드할 준비가 모두 끝났습니다.
- git push origin main
    - 깃허브의 main 브랜치에 업로드 한다는 의미입니다.
    - 이전에 add 하여 목록에 추가시킨 파일이 업로드되고, commit -m 을 통해 작성한 메시지가 등록됩니다.

<aside>
💡 해당 명령어들은 업로드할 때마다 쓰이니까, 손에 익히는 게 좋습니다 !

</aside>

### git pull - 깃허브와 컴퓨터의 버전 맞추기

- 우리는 협업을 하고 있으니까, 만약 다른 사람이 개발을 열심히 해서 깃허브에 업로드를 했다면 ?
- 깃허브에 업로드가 되어있지만, 자신의 컴퓨터에는 반영이 되지 않은 상태입니다.
- git pull 이라는 명령어를 사용하면, 깃허브의 최신내용을 반영해줍니다 !

### 요약

1. git clone 주소, 입력하여 내 컴퓨터에 저장하기
2. 코드를 열심히 짜기
3. git add .   /   git commit -m “작업내용” / git push origin main  하여 깃허브에 업로드 하기
4. 주기적으로 git pull 하여 최신 상태를 유지하기 

## 심화, 협업 내용

실제로 협업을 하다보면 발생할 수 있는 문제점을 방지할 방법입니다.

제가 동아리에서 사용한 방법인데, 정답은 아닐 수 있습니다. 

### 브랜치란 ?

<img width="833" alt="Untitled 1" src="https://github.com/Project-Division/about_react/assets/68108664/5c6b9c73-319c-4ce7-952d-278cb8eb77c2">

- 이런식으로 메인 저장소를 그대로 둔 채, 별도의 작업 공간을 만드는 것을 의미합니다.

<img width="267" alt="Untitled 2" src="https://github.com/Project-Division/about_react/assets/68108664/605865c7-5b8e-4eed-973c-b1d4c16a4e0e">

- 깃허브 사이트에서 브랜치를 생성할 수 있습니다.

<img width="478" alt="Untitled 3" src="https://github.com/Project-Division/about_react/assets/68108664/2d5e4bb4-76fa-4a73-ae7e-f33c09429f94">

- 해당 페이지에서 브랜치를 생성할 수 있습니다.
- source 는 어떤 브랜치에서 뻗어나갈 것인지 결정하는 것입니다. 예를 들어 main 을 선택하면, 현재 main 브랜치의 내용을 그대로 가져온 상태로 작업할 수 있습니다.
- source 는 협업하는 사람들이 모두 업로드 하는 공간을 선택하면 됩니다.

<img width="323" alt="Untitled 4" src="https://github.com/Project-Division/about_react/assets/68108664/c6eb4fc0-7127-4bad-8969-f9c0fea55992">

- 이제 자신의 브랜치가 생성되었습니다.

### 브랜치를 나누는 이유

- 우리는 함께 작업을 하고 있습니다. 동일한 저장소에 여러명이 업로드 하는 경우 에러 (충돌) 가 발생할 수 있습니다.
- 그리고 다른 사람이 업로드하고 난 이후 자신이 업로드를 하려한다면, 자신의 파일 내용들이 반영되기 때문에 이전에 업로드 했던 내용들이 사라질 수 있습니다.
- 따라서 주기적으로 git pull 명령어를 사용하는 것이 필요하기도 합니다. (최신화 유지)

### 다른 브랜치에 push 하는 방법

- 기초 내용에서 git push origin main  은 main 브랜치에 업로드하는 것이라 작성해두었습니다.
- 마찬가지로 만약 example 이라는 브랜치를 생성했다면, git push origin example 이라 하면 example 브랜치로 업로드할 수 있습니다.

- 그러나 본인의 로컬저장소 (pc 저장소) 는 브랜치가 만들어진걸 모르고 있겠죠 ?
- 깃허브에 다른 브랜치를 생성했으면, 본인 컴퓨터와 일치시켜주는 작업이 필요합니다.

- 그냥 push 하려고 하면 이러한 결과가 발생합니다.

<img width="533" alt="Untitled 5" src="https://github.com/Project-Division/about_react/assets/68108664/2acfd1e0-62bc-4036-9770-93fb168639e3">

- example 브랜치와 일치하지 않는다는 에러입니다.

- git checkout -b example 이라는 명령어를 사용하면, example 이라는 브랜치로 이동합니다.

<img width="670" alt="Untitled 6" src="https://github.com/Project-Division/about_react/assets/68108664/d48a8ce0-3e4d-4da7-b01b-bc6266a9e49c">

- 이제 브랜치명이 일치하므로 업로드 하는데에 성공합니다.

### pull request

- 우리의 주된 목적은 충돌방지입니다. pull request 는 코드를 업로드하기 이전에 ‘합쳐도 될까요?’ 묻는 장치라고 생각하면 됩니다.
- 우리는 main 브랜치에 최종 코드를 업로드 해야하며, 지금은 자신만의 브랜치에 작업한 결과를 올린 것입니다.
- 앞서 작성한 것처럼 example 이라는 브랜치에 업로드를 하고 나서 깃허브에 접속하면 이런 화면을 볼 수 있습니다.

<img width="622" alt="Untitled 7" src="https://github.com/Project-Division/about_react/assets/68108664/8413d804-6255-4608-8f44-c96d0fd22848">

- example 브랜치에 새로 업로드 된 내용이 있는데, 비교하고 pull request 를 쓸건지 물어보는 버튼이 생깁니다.
- 해당 버튼을 누르면 지금 충돌이 날지 파악하고, 코드 통합을 요청할 수 있는 창으로 이동됩니다.

<img width="484" alt="Untitled 8" src="https://github.com/Project-Division/about_react/assets/68108664/d6b04755-141e-4ce5-96a2-3b562c3ef20e">

- able to merge → 지금 병합해도 충돌이 나지 않는단 의미입니다.
- 해당 입력 form 에 작업한 내용을 상세히 작성할 수 있습니다.

### merge

- 이제 다른 사람들이 협업한 코드를 합치려고 합니다.
- pull request (합쳐도 되는지 요청이 들어온 것) 을 수락하면 코드를 합칩니다.

<img width="613" alt="Untitled 9" src="https://github.com/Project-Division/about_react/assets/68108664/f9653112-8ae9-450a-a863-445161f3c09f">

- 깃허브의 pull request 에 들어가면 통합 요청들이 표시됩니다.
- 그 중 하나를 눌렀을 때의 예시 화면입니다.
- 해당 사람이 어떤 작업을 했는지, 코드에 어떤 변동사항이 있는지 표시됩니다.

- 코드를 읽어보고 병합해도 되겠다 싶으면 merge pull request 버튼을 눌러 수락하면 됩니다.
- 그러면 main 브랜치에 코드가 통합됩니다.

### 요약

1. 동일한 저장소에 여러명이 접근하면 충돌이 발생할 수 있다. 
2. 그래서 ‘브랜치’ 라는 시스템을 통해 동일한 파일을 두고 각자 작업을 할 수 있다
3. 따라서 업로드할 때, 우선 자신의 브랜치에 업로드를 수행한다
4. 깃허브에서 메인 저장소와 통합을 요청한다
5. 코드를 통합하는 사람이 코드를 점검하고 통합을 수락한다.