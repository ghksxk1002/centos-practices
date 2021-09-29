# centos7 Java 설치

#### 1.Java JDK 다운로드

```
wget  jdk-8u291-linux-x64.tar.gz
```



#### 2.linux 서버(root 홈디렉토리)에 업로드 하기

: 작업 디렉토리는 /root (root 홈)

1.압축을 푼다.

```
tar xvfz jdk-8u291-linux-x64.tar.gz
```

2.더존 소프트웨어 설치 디렉토리 만들기

```
mkdir /usr/local/douzone
```

3.만들어진 더존 디렉토리 밑에 설치

```
mv jdk1.8.0_291 /usr/local/douzone/java1.8
```

4.링크 파일 생성

> 자바버전을 수정하기 수월

```
ln -s /usr/local/douzone2021/java1.8 /usr/local/douzone/java
```

![자바링크드파일 만든후](C:\Users\user\Desktop\자바링크드파일 만든후.PNG)



5.환경변수설정(/etc/profile)

> centos가 PATH를 보고 자바를 실행해줌

```
# java
export JAVA_HOME=/usr/local/douzone2021/java
export CLASSPATH=$JAVA_HOME/lib/tools.jar
export PATH=$PATH:$JAVA_HOME/bin
```

8. 현재 shell 환경에 적용하기

```
source /etc/profile
```

9. 확인 작업

```
java -version
```

> java version "1.8.0_291"
> Java(TM) SE Runtime Environment (build 1.8.0_291-b10)
> Java HotSpot(TM) 64-Bit Server VM (build 25.291-:ㅂ10, mixed mode)

![자바버전확인](C:\Users\user\Desktop\자바버전확인.PNG)