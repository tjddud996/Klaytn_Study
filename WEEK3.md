# Klaytn-study-3
## 섹션4_클레이튼 덧셈게임 개발 프론트엔드

### 1. 환경설정

#### 1) 다운받아야 할 파일
> Node.js
  - 서버 사이드 자바스크립트 플랫폼
  - https://nodejs.org/en/ 여기서 다운

> NPM
  - Node.js를 설치하면 같이 설치됨
  - 개발하면서 툴이나 라이브러리를 다운받기 위해 꼭 필요

> 트러플 프레임워크
  - NPM을 통해 다운받음
  - Bapp을 쉽게 개발할 수 있게 해주는 프레임 워크
  - 스마트계약을 컴파일하고 테스트하며 배포도 할 수 있게 해줌

> 비주얼 스튜디오 코드

#### 2) 환경설정 코드

- 파워쉘을 열어서 node -v로 잘 설치되었는지 확인
- npm -v : npm 버전 확인
- npm uninstall -g truffle : 트러플 프레임 워크 이전 버전 삭제
- npm install -g truffle@4.1.15 : 트러플 프레임워크 버전 4.1.15 설치
- truffle cmd version : 트러플 버전 확인

#### 3) 비주얼 스튜디오 코드 다운
- Solidity : 스마트 계약을 작성할 수 있는 프로그래밍 언어
- https://code.visualstudio.com/ 여기서 비주얼스튜디오 코드 다운
- Solidity Extension 설치 -> Solidity 문법마다 강조되는 색깔을 제공


### 2. boilerplate 받기
- 트러플 박스 : 트러플에서 Bapp개발에 필요한 표준 템플릿을 다운받게 해주는 곳
- git clone https://github.com/kkagill/addtion-game-starter.git : 파일 설치한 후 다음으로 깃헙에서 파일 다운
- code . : 비주얼 스튜디오 코드로 염

#### 비주얼 스튜디오 코드설명
- Contracts : Solidity 컨트랙트 파일들을 보관하는 곳
- AdditionalGame.sol : 우리가 만들어 놨던 컨트랙트 파일
- Migrations.sol : 스마트 계약을 배포할 때 아래 있는 migrations폴더 안에 있는 스크립트 파일들을
실행
- 1_initial_migration.js : 배포하는 과정에 쓰이는 로직이 담겨있음, migration 컨트랙트 파일을 가져와서
그 내용을 클레이튼 노드에 deploye(배포)를 함

- src폴더 안에는 Bapp의 프론트엔드를 담당하는 구조를 설정
- index.html파일 : view를 담당, Bapp에 쓰일 jquery나 bootstrap을 cdn으로 불러옴
- index.js파일 : 기능들을 실행하기 위한 엔진과 같은 파일, 사용할 함수들 이름들만 정의
- package.json : npm을 통해 필요한 dependency를 추가하는 부분
- caver-js : 클레이튼 블록체인과 소통하게 해주는 라이브러리 파일
- truffle.js : 환경설정을 담당, 어느 네트워크에 스마트 계약을 배포할 지 여기에 정의
- webpack.config.js : 파일들을 최적화시켜주고 코드에 변화가 있을 때마다 감지를 해서 브라우저의
변경사항을 새로고침할 필요 없이 반영해주는 역할


### 3. Baobab에 스마트 계약 배포1
- 비주얼 스튜디오 코드에서 Terminal > New Terminal로 새 터미널을 염
- npm install : npm을 설치

#### ※※※※여기서 부터 npm이 제대로 설치되지 않는 오류 발생※※※※

### 번외. npm install 오류 해결
> 윈도우 환경에서 실행하지 않고 ubuntu 환경에서 실행하도록 한다.

#### 1) 윈도우에 ubuntu 설치할 수 있는 환경 설정
- 제어판 > 프로그램 > 프로그램 및 기능 > Windows 기능 켜기/끄기
- 'Linux용 Windows 하위 시스템' 체크박스 클릭
- 컴퓨터 재부팅

#### 2) ubuntu 설치
- Microsoft store에서 linux검색 후 “windows에서 linux 실행하기” 클릭
- ubuntu 클릭 후 다운로드

#### 3) ubuntu 실행
- 다운로드 받은 ubuntu 실행
- username 입력
- password 입력
- 설치 완료

* cmd 창에서 bash 입력 시 우분투 터미널 이용 가능

#### 4) 업데이트
- sudo apt-get update
- sudo apt-get upgrade > YES 선택

#### 5) node.js, npm 버전 확인
- node -v : node.js 버전 확인
- npm -v : npm 버전 확인
= Command not found 오류 발생

#### 6) 오류 해결
- curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash –
- sudo apt-get install -y nodejs
- sudo apt install note
- sudo apt-get install -y build-essential

#### 7) node.js, npm 버전 재확인
- node -v : node.js 버전 확인
- npm -v : npm 버전 확인
= npm만 Command not found 오류 발생

#### 8) npm 버전 오류 해결
- sudo apt install npm
- npm -v
= 제대로 된 버전 확인!

#### 9) npm install
- 비주얼 스튜디오 코드에서 new Folder로 코드 파일이 있는 폴더 열기
- Terminal > New Terminal로 새 터미널을 염
- bash로 ubuntu 터미널 진입
- npm install

#### 성공!
