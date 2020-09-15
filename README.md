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
