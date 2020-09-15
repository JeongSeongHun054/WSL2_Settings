# WSL2_Settings

## Windows 2004 Version Update
## 필수 소프트웨어 설치
    - Chrome
    - VSCode
    - Git(기본 설정 그대로)
#### VSCode 설치 시 주의사항! 해당 체크 꼭 

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/vscode%EC%82%AC%EC%A7%84.PNG" alt="logo"/></a>

## VSCode CustomMizing
    - Extension 설치!
        - ESLint
        - Prettier
        - Material theme
        - Material Icon Theme

## Chocolatey? Window 환경에서 Mac처럼 Terminal에서 파일을 Install 하게 도와주는 것!!
    
### PowerShell을 관리자 권한으로 실행

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/powershell.png" alt="logo"/></a>

#### 아래 명령어 복사 후 붙여넣어서 Chocolately 다운로드, 완료 후 PowerShell 재부팅

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))



<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/choco.PNG" alt="logo" /></a>


### chocolatey.org/packages 에서 프로그램별 명령어 확인

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/choco2.PNG" alt="logo" /></a>


## Chocolatey를 이용한 Python 설치, 완료 후 PowerShell 재부팅, python 명령어 입력 후 확인 
    choco install python

## Chocolatey를 Terminal 설치
    choco install microsoft-windows-terminal
<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/terminal.PNG" alt="logo" /></a>

## Linux 환경을 쓰지 않고 Windows를 쓴다면 여기까지만 진행!!!!

## Windows Subsystem for Linux(WSL) 추가

- Windows Terminal을 관리자 권한으로 실행 & 아래 명령이 입력

        dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    
<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/wsl.PNG" alt="logo" /></a>

## Microsoft Store에서 Ubuntu 18.04(마음에드는 Version) 설치 && 컴퓨터 재시작

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu.PNG" alt="logo" /></a>

## Ubuntu 실행 후 설치 대기

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu2.PNG" alt="logo" /></a>

## Linux 사용을 위한 계정입력 후 설치완료

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu3.PNG" alt="logo" /></a>

## WSL2로 Update

- 관리자 권한으로 Terminal 실행 후 아래 코드 입력 && 설치 완료 후 컴퓨터 재시작

        dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
        
<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu4.PNG" alt="logo" /></a>

- 기본 버전을 WSL2로 설정

        wsl --set-default-version 2
        
- 만약 이런 메세지가 뜬다면 커널 업데이트

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu5.PNG" alt="logo" /></a>


### https://aka.ms/wsl2kernel 에 들어가서 아래 링크 클릭

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu6.PNG" alt="logo" /></a>

- 다시 명령어 실행 후 확인

        wsl --set-default-version 2

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu7.PNG" alt="logo" /></a>

## Ubuntu에서 WSL2를 사용할 수 있도록 설정

### 아래 명령어로 Ubuntu 이름 확인

    - wsl --list --verbose
    
<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu8.PNG" alt="logo" /></a>

### Ubuntu에 WSL2를 사용하도록 설정
    
    - wsl --set-version Ubuntu-18.04 2
    
## Terminal 커스텀마이징

### Ubuntu에서 설정 진입 && 만약 The 'Remote-WSL' extension이 나오면 설치!

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu11.PNG" alt="logo" /></a>
