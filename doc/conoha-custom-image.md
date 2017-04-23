# ConoHa 커스텀 이미지 올리기

## conoha 콘솔

Ubuntu 64비트로 설치 하였습니다. root 접속

`Login incorrect` 발생시, `텍스트 전송`을 통해서 암호를 입력합니다.

### vsftpd 패키지 설치

```sh
apt-get install vsftpd
``` 

### 사용자 추가

```sh
adduser ftpuser
```

### conf 수정

```sh
nano /etc/vsftpd.conf
```

write_enable=YES 부분의 주석을 삭제한다.

### 서비스 재시작
```sh
service vsftpd restart
```
### 파일 전송

FileZilla 등 프로그램을 통해서 ftp 접속

ISO 파일을 전송한다.

## web server 설치

### update & upgrade

```sh
apt-get update
apt-get upgrade
```

### Apache2 설치

```sh
apt-get install apache2
```

아이피로 접속해서 웹 페이지가 정상적으로 나오는지 확인합니다.


## ISO 전송하기

```sh
cd /var/www/html
wget [WINDOWS.ISO_URL]
```

url 정보가 입력되지 않으면 `텍스트 전송` 메뉴를 통해서 입력합니다. 


## 출처
- http://goproprada.tistory.com/189
- https://blog.lael.be/post/73

