# NAVER Cloud Platform with NodeJS

- [Naver Cloud Platform](https://www.ncloud.com/)

    > Naver Cloud Platform - 이하 nbp - 는 가상의 클라우드 웹서버를 제공하는 서비스입니다.

## 01. Server 생성

> 본 내용은 이미 해당 서비스에 가입은 완료하신 상태로 가정하며, 최대한 리눅스를 접해보지 않으신 분도 이해하실 수 있도록 다소 설명이 과할 수 있습니다.

<br>

- Console 버튼 클릭

    [Naver Cloud Platform](https://www.ncloud.com/) 링크로 들어가시면 우측 상단에 Console 버튼이 있습니다. 이를 클릭하여 다음 페이지로 접근합니다.
<p align="center">
    <img src="https://github.com/cliche90/nbp_guide/blob/master/images/01.PNG?raw=true">
</p>
<br></br>

- Server 메뉴 선택

    좌측에 Server 탭 - Server를 선택합니다.(기본값으로 지정되어 있음)

<p align="center">
    <img src="https://github.com/cliche90/nbp_guide/blob/master/images/02.PNG?raw=true">
</p>
<br></br>

- 서버 생성 버튼 클릭

    해당 탭에서 서버생성 버튼을 눌러 서버 생성 과정을 진행합니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/03.PNG?raw=true">
</p>
<br></br>

- 서버 생성 진행

    > 인증키가 있는 경우에는 그대로 진행하시면 되고, 없으실 경우에는 생성하셔서 pem 파일을 별도로 만드시면 됩니다.

    1. 서버 생성에서는 첫번째 페이지에서 원하는 스펙을 선택하시고 끝까지 다음버튼을 눌러 진행합니다.
    2. 서버이름은 임의로 설정하시면 됩니다.
    3. acg의 경우 추후 수정할 것이지만 우선 기본값으로 설정하고 진행합니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/04.PNG?raw=true">
</p>
<br></br>

- 서버 생성 완료

    진행이 완료되면 아래 이미지처럼 생성된 서버를 확인할 수 있습니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/05.PNG?raw=true">
</p>
<br></br>

## 02. Public IP 할당

- 공인 IP 탭 선택

    서버 생성 후 해당 서버에 접근하기 위해서는 공인 IP가 필요합니다. 좌측에서 Public IP 탭을 찾아 선택합니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/06.PNG?raw=true">
</p>
<br></br>

- 서버 선택 후 서버에 할당 버튼 클릭

    Public IP 탭을 선택하면 이전 생성했던 서버가 리스트에 출력되고 이를 선택하면 체크박스가 체크됩니다. 이 상태에서 서버에 할당 버튼을 누릅니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/07.PNG?raw=true">
</p>
<br></br>

- 할당

    추가한 서버의 이름을 선택하고 할당 버튼을 누르면 공인 IP가 할당됩니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/08.PNG?raw=true">
</p>
<br></br>

- 할당 완료

    이미지 상에는 지워져 있으나, 적용서버 부분에 서버의 이름이 표시되고, 여기의 공인 IP를 통해 외부에서 접근이 가능하도록 공인 IP 할당이 완료됩니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/09.PNG?raw=true">
</p>
<br></br>

## 03. ACG 수정

> 기본적으로 리눅스 기준으로 22번 port는 ACG 항목에 추가되어 있으나, 서버 접속에 앞서 확인 겸 ACG 수정을 먼저 진행합니다.

- ACG 탭 선택

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/10.PNG?raw=true">
</p>
<br></br>

- ACG 설정 버튼 클릭

    초기 서버 생성시에 기본값으로 진행하셨다면, 아래의 이미지와 같이 ncloud-default-acg가 acg로 설정되어 있을 것입니다. 이를 선택하시고 ACG 설정 버튼을 클릭합니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/11.PNG?raw=true">
</p>
<br></br>
    
- ACG 설정 내용

    내용은 차이가 있을 수 있습니다. 제 경우에는 ssh접근을 위한 22번 포트와 노드를 올릴 3000번 포트만 오픈하도록 설정하였습니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/12.PNG?raw=true">
</p>
<br></br>

## 04. 서버 계정 및 비밀번호 확인

- 서버 탭 선택

    맨 처음 서버 생성시 선택하셨던 탭을 선택합니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/01.PNG?raw=true">
</p>
<br></br>

- 서버 관리 및 설정 변경 버튼 클릭 - 관리자 비밀번호 메뉴 선택

    서버를 선택하신후 리스트의 상단에 있는 서버 관리 및 설정 변경 버튼을 클릭하시고 여기에서 나타나는 메뉴들 중 관리자 비밀번호 메뉴를 선택합니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/13.PNG?raw=true">
</p>
<br></br>

- 인증키 파일 선택

    서버 생성시 작성하셨던 pem 파일을 선택하시고, 비밀번호 확인 버튼을 누릅니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/14.PNG?raw=true">
</p>
<br></br>

- 비밀번호 확인

    여기까지 진행하시면 서버의 이름과 root 계정, 임시로 발급되어 있는 비밀번호를 확인하실 수 있습니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/15.PNG?raw=true">
</p>
<br></br>

## 05. SSH를 통한 서버 접근

> 이전 과정에서 획득한 root 계정과 비밀번호를 통해 서버에 접근할 수 있습니다. putty 등의 툴을 사용하셔도 좋고, 저는 bash on ubuntu on windows를 사용하고 있으므로 bash의 ssh 커맨드를 이용하여 접근하겠습니다.

- Public IP 확인 및 접속

    서버 탭에서 추가한 서버 내용을 보시면 리스트의 항목 중 공인 IP 부분을 확인하실 수 있습니다. acg에서 22번 포트를 열어두었으므로, 아래의 커맨드를 통해 서버에 접근합니다.

        ~$ ssh root@[공인 IP]

    현재 과정까지 정상적으로 이루어졌다면, 해당 커맨드 이후 비밀번호를 요구할 것이고, 여기서 이전과정에서 확인했던 임시 비밀번호를 입력합니다.

    접속이 정상적으로 이루어졌다면 __[root@서버이름 ~]#__ 과 같이 서버에 접속될 것입니다. 임시 비밀번호는 혼동하기 쉬우니 커맨드 창에서 `passwd` 커맨드를 입력하여 새로운 비밀번호로 변경해 주는 편이 좋습니다.

## 06. NodeJS 파일 작성

> 테스트를 위한 파일이므로 node와 express만 설치하여 확인하도록 하며, 이에 대한 더 자세한 내용은 범주를 넘어서므로 소개하지 않도록 하겠습니다.

- 소스코드를 작성하기에 앞서 node와 npm을 설치해야 합니다.

    해당 과정은 [NodeJS의 공식 페이지](https://nodejs.org/ko/download/package-manager/)에 잘 설명되어 있습니다. 저의 경우는 CentOS 기준으로 작성하였으므로 패키지 관리자를 통해 설치할 수 있도록 아래의 커맨드를 이용합니다.

        curl --silent --location https://rpm.nodesource.com/setup_6.x | bash -
        yum -y install nodejs

- 설치가 종료되면, 별 이상없이 nodejs가 설치되어있는지 확인하기 위해 아래 커맨드를 입력하여 nodejs의 버전을 확인합니다.

        node -v

- nodejs와 npm이 설치되었으므로, 저희가 사용하고자 하는 node package 중 하나인 express를 설치합니다. init을 할 때에는 기본값으로 해도 문제가 없으므로, 모두 엔터를 쳐서 넘겨줍니다.

        npm init
        npm install express --save

- 아래의 커맨드를 이용하여 파일을 여시고 소스코드를 작성해 주세요.

        vi app.js
        // i를 눌러 입력 모드로 변경
    >
        var express = require('express');
        var app = express();

        app.get('/', function(req, res){
            res.send('Hello NAVER Cloud Platform!!');
        });

        app.listen(3000, function(){
            console.log('Connected!!');
        });
        // 작성 완료 후 ESC키를 누르고 :wq 그리고 엔터 키를 눌러 파일을 저장하고 vim을 빠져나옵니다.

- 이제 NodeJS를 통해 작성한 app.js 파일을 실행시킵니다.

        node app.js

    별 문제 없이 진행하셨다면 위해서 작성했듯이 'Connected!!' 라는 텍스트를 콘솔 창에서 확인하실 수 있으실 것이고, 이제 브라우저를 통해 작성한 웹 페이지를 볼 수 있게 되었습니다.
    
    브라우저를 통해 `http://[공인IP]:[PORT]`로 접근하시면 app.js에서 브라우저로 보냈던 'Hello NAVER Cloud Platform!!' 라는 문구를 확인하실 수 있습니다.
    
    저는 3000번 포트를 Listen하도록 해 두었고, ACG에도 3000과 22번 포트만 오픈해 두었으니 포트에는 3000 포트를 입력해야 접속할 수 있습니다.

<p align="center">
    <img style="margin-left:auto; margin-right:auto; display:block;" src="https://github.com/cliche90/nbp_guide/blob/master/images/16.PNG?raw=true">
</p>