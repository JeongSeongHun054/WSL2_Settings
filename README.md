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

### Windwos Terminal의 기본 Terminal을 ubuntu로 변경

- Ubuntu 18.04에 있는 "guid"의 값을 "defaultProfile"에 넣기

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu12.PNG" alt="logo" /></a>

### Ubuntu Terminal에서 oh my zsh 설치

- zsh 설치

        sudo apt install zsh
        
- oh my zsh 설치
            
        sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
        
- zsh를 기본 shell로 사용한다고 Y 입력 후 설치 완료

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu13.PNG" alt="logo" /></a>

### Ubuntu Terminal에 Powerlevel10K 적용시키기

- Terminal 설정에서 "schemes"에 해당 color들 추가

```
{"name": "vscode", "background" : "#232323","black" : "#000000","blue" : "#579BD5","brightBlack" : "#797979","brightBlue" : "#9BDBFE","brightCyan" : "#2BC4E2","brightGreen" : "#1AD69C","brightPurple" : "#DF89DD","brightRed" : "#F6645D","brightWhite" : "#EAEAEA","brightYellow" : "#F6F353","cyan" : "#00B6D6","foreground" : "#D3D3D3","green" : "#3FC48A","purple" : "#CA5BC8","red" : "#D8473F","white" : "#EAEAEA","yellow" : "#D7BA7D"}
```

- Terminal에서 "profiles" 에 "defaults" 코드 추가

        "colorScheme": "vscode"

- powerlevel10k 설치

        sudo git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

- .zshrc 파일 수정(아래 코드 입력)

        code ~/.zshrc
    
- ZSH_THEME 코드를 찾아서 아래와 같이 수정

        ZSH_THEME="powerlevel10k/powerlevel10k"
        
- 제일 밑에 아래 코드 추가
        
        [[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
        LS_COLORS="ow=01;36;40" && export LS_COLORS

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu15.PNG" alt="logo" /></a>

- Ubuntu Terminal 확인!
    1. Terminal에 나오는 모양이 다르다면?
    2. MesloLGS NF 폰트 설치 후 아래 과정 진행

- Terminal 설정에서 Font 적용(MesloLGS NF), "profiles" 에 "defaults" 코드 추가

        "fontFace": "MesloLGS NF"
    

- VSCode에서도 Font 적용
    
    1. Ctrl + , 눌러서 VSCode 설정 진입
    2. Terminal > Intergrated: Font Family에 MesloLGS NF 적용
    3. intergrated terminal 입력 후 Terminal > Integrated > Shell: Windows 찾기
    4. Edit in settings.json 클릭
    5. 아래 코드 입력
        ``` "terminal.integrated.shell.windows": "C:\\windows\\System32\\wsl.exe" ```
- powerlevel10k 설치 계속 진행

        1. (3)번으로 진행

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu17.PNG" alt="logo" /></a>

        2. 나머지 계속 진행
       
## 설치완료

<a href="#"><img src="https://github.com/JeongSeongHun054/WSL2_Settings/blob/master/ubuntu18.PNG" alt="logo" /></a>

- 만약 powerlevel10k를 다시 설정하고 싶다면? 아래 코드 
        
        p10k configure

## python 기본 version 설정

1. code ~/.zshrc
2. 제일 하단에 ``` alias python=python3.9 ``` 추가

## NVM 설정
- nvm이란? Node 버전을 관리하게 해주는 것. 아래 코드로 설치 후 Terminal 재시작

        curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

- ~/.zshrc 제일 하단에 아래 코드를 추가하여 zsh에서 NVM을 인식하도록 함.

        export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
        [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
- 사용법
    - nvm ls-remote를 통해서 사용가능한 모든 NodeJS 버전확인 LTS(Long-Term-Support) 사용 권장
        - LTS 버전만 보고싶다면?
            ``````
    - 다른 버전을 사용하고 다운받고 싶다면? Version 명을 통해서 설치
    
        ```nvm install v10.21.0``` 
        
    - 다운로드 되어있는 다른 버전의 NodeJS를 사용하고 싶다면?
    
        ```nvm use v12.18.2```
        
    
