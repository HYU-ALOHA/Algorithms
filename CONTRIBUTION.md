# 기여하는 법
본 문서는 해당 레포지토리에 대해 초심자들이 첫 기여를 간단하게 할 수 있도록 가이드라인을 제시하고자 합니다.

## Fork
레포지토리 페이지 우측 상단에 **Fork** 버튼을 찾을 수 있습니다. 클릭하면, 본인의 계정에 이 레포지토리의 복사본을 생성하게 됩니다.

## Clone
새롭게 본인의 계정에 생성된 복사본 레포지토리를 이제 본인의 기기로 clone하면 됩니다. 본인의 계정 페이지로 가서, fork된 복사본 레포지토리를 열고, **Code**버튼을 누르면 clone을 위한 다양한 옵션들을 확인할 수 있습니다.  
Git이나 CLI가 익숙하지 않으신 분들은 **Github Desktop**을 설치하고, Code버튼을 누른 후 드롭다운에서 Open with GIthub Desktop 옵션을 선택하여 진행하면 됩니다.

다양한 방법이 있지만, HTTPS 링크를 활용한 방법을 소개하겠습니다.
레포지토리를 본인 기기에 설치하고 싶은 경로에서 터미널을 열고, 아래와 같은 형태의 git command를 입력하시면 됩니다.
```git
git clone https://github.com/this-is-you/Algorithms.git
```
여기서 `this-is-you`에 본인의 GitHub 이름을 입력하시면 됩니다. 이렇게 함으로써 fork해온 레포지토리의 내용물을 본인의 기기에 복사받을 수 있습니다.

## Branch 생성
이제 생성한 레포지토리 안쪽으로 진입합시다.
```
cd Algorithms
```
이제 `git checkout` 커맨드를 사용해 새로운 Branch를 만들어 봅시다.
```
git checkout -b new-branch-name
```
예를 들어:
```
git checkout -b add-work
```
(Branch의 이름은 본인 마음대로 작성하면 되지만, 해당 branch의 목적이 잘 드러나도록 이름을 짓는 것이 좋습니다.)

## 변경 후 Commit
이제 본인이 기여하고자 하는 바대로 알고리즘 소스 코드 파일을 추가하거나, 기존 파일의 문제점을 수정하거나, 새로운 Documentation을 추가하거나 등의 변경 작업을 수행하면 됩니다. (파일의 세부 양식은 해당 문서를 따로 참고해주시기 바랍니다.) **특히 변경된 directory의 README.md 파일이 업데이트가 필요한 경우 반드시 그에 따라 업데이트 해주시기 바랍니다.**

이제 해당 프로젝트 경로에서 `git status`커맨드를 실행하면, 어떤 변경사항들이 있었는지 알 수 있을 겁니다.
해당 변경사항들을 `git add`커맨드를 통해 아까 만들었던 branch에 추가해줍시다.
```git
git add "추가하거나 변경한 파일 이름"
```
이제 이 변경사항들을 `git commit`커맨드를 통해 commit해줍시다.
```git
git commit -m "변경사항에 대한 commit 메세지"
```

## Github에 변경사항 push하기
`git commit`을 통해 본인의 로컬 기기에는 변경사항들이 저장되었지만, GitHub 원격 저장소에는 해당 변경사항들을 아직 업데이트해주지 못했습니다.  

`git push`커맨드를 통해 이러한 변경사항들을 원격 저장소로 push해줍시다.
```git
git push origin <branch 이름>
```
여기서 `<branch 이름>` 부분을 아까 지었던 branch의 이름으로 대체해주시면 됩니다.

## 변경사항 제출하고 review받기
이제 GitHub에서 fork해서 생성했던 본인의 레포지토리로 가보면, 새로운 `Compare & pull request` 버튼이 보일 겁니다. 말 그대로 원본 레포지토리와 변경사항들을 비교하고, 이러한 변경사항들을 원본 레포지토리로 보내고자 하는 pull request를 생성하는 버튼입니다. 클릭해 봅시다.

양식에 따라 pull request에 대한 내용들을 작성하고, `Create pull request`버튼을 통해 pull request를 생성하면 끝입니다. 이제 원본 레포지토리의 관리자들이 해당 pull request의 내용들을 review하고, 문제가 없다고 판단되면 원본 프로젝트의 master branch로 merge하게 됩니다. merge가 일어날때 해당 사항에 대한 알림 메일을 받을 수 있습니다.

## 축하합니다!
프로젝트 기여자로서 자주 경험하게 될 일반적인 *fork -> clone -> edit -> pull request* workflow를 방금 완료하셨습니다. 이를 숙지하고 익숙해진다면 이후 다양한 프로젝트에 더욱 손쉽게 기여할 수 있을 것입니다.