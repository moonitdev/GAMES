
## git
### 원격 저장소 생성
- [moonitdev github](https://github.com/moonitdev)
- [GAMES repository](https://github.com/moonitdev/GAMES.git)

### 로컬 저장소 생성(git clone)
```
projects> git clone https://github.com/moonitdev/GAMES.git
projects> cd GAMES
```

### 프로젝트 폴더 생성
```
projects\GAMES> mkdir test
projects\GAMES> cd test
```

### (빈) 파일 생성
- test/_flask_chat.bat 생성
```bash
mkdir flask-chat-simple
cd flask-chat-simple
type NUL > .env
type NUL > app.py
type NUL > namespaces.py
mkdir src
type NUL > src/index.html
type NUL > src/index.css
type NUL > src/index.js
```

- test/_flask_chat.bat 실행
```cmd
projects\GAMES\test> _flask_chat.bat
```

### 가상 환경 생성

```
# Create virtual ENV.
projects\GAMES\test\flask-chat-simple> virtualenv .venv
 
# Activate virtual ENV.
### for Windows
projects\GAMES\test\flask-chat-simple> .venv\Scripts\activate
 
### for Linux/OSX
. .venv/bin/activate
```

### 라이브러리 설치

```
projects\GAMES\test\flask-chat-simple> pip install flask python-socketio python-dotenv
```

### 환경변수 설정
- flask-chat-simple/.env
```
FLASK_MODE=development
FLASK_DEBUG=1
```

### 파일 편집



### 실행
```
(.venv) projects\GAMES\test\flask-chat-simple>python app.py
```

python-engineio 4.0.0
python-socketio 5.0.4


!BUG
 ERROR in server: The client is using an unsupported version of the Socket.IO or Engine.IO protocols (further occurrences of this error will be logged with level INFO)


### index.html
```
https://cdnjs.cloudflare.com/ajax/libs/socket.io/2.2.0/socket.io.js
https://cdnjs.cloudflare.com/ajax/libs/socket.io/3.0..4/socket.io.js
```

### 라이브러리 다운그레이드
```
pip uninstall python-socketio
pip install python-socketio==4.3.0
```

### !BUG: 전과동!!!



[socket.io Version compatibility](https://python-socketio.readthedocs.io/en/latest/intro.html)

JavaScript Socket.IO version	Socket.IO protocol revision	Engine.IO protocol revision	python-socketio version	python-engineio version
0.9.x	1, 2	1, 2	Not supported	Not supported
1.x and 2.x	3, 4	3	4.x	3.x
3.x	5	4	5.x	4.x

!SOL
### fix version 
python-engineio: .2.0
python-socketio: 4.2.0
JavaScript socket.io: 2.2.0


### 방화벽 인바운드 설정

네트워크 및 인터넷 > 상태 > Windows 방화벽 > 고급 설정
인바운드 규칙 > 새 규칙 > 3000-9000 개방