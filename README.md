# My WSL Settings

## Windows에서

### Windows Terminal 설치

- Mircrosoft Store에서 설치

### WSL 활성화

```(bash)
# cmd or powershel
wsl --install
```

### 폰트 설치

- [폰트 다운로드](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf) 받은 후 설치

### Windows Terminal 폰트 설정

- 설정에서 왼쪽 하단 톱니바퀴 아이콘을 눌러 JSON 파일을 다음과 같이 수정

```(json)
"profiles":
    {
        "defaults": {
            "fontFace": "MesloLGS NF",
            "fontSize": 10
        },
    ...
    }
```

---

## WSL(Ubuntu)에서

### zsh 설치

```(bash)
sudo apt-get install zsh
```

### oh-my-zsh 설치

```(bash)
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Plugin 설치

##### zsh-autosuggestion

```(bash)
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

##### zsh-syntax-highlighting

```(bash)
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
```

### Shell 설정 수정

```(bash)
vi ~/.zshrc
```

##### 다음과 같이 수정

```
plugins=(
 	    git
    	zsh-autosuggestions
    	zsh-syntax-highlighting
 )
```

##### 수정사항 적용

```(bash)
source ~/.zshrc
```

### 테마 설치

```(bash)
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

### 테마 적용

```(bash)
vi ~/.zshrc
```

##### 다음과 같이 수정

```
ZSH_THEME="powerlevel10k/powerlevel10k"
```

##### 수정사항 적용

```(bash)
source ~/.zshrc
```

##### 뜨는 화면에서 본인 취향에 맞게 설정
