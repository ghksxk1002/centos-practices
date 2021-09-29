# centos-practices

####1. Java JDK 다운로드
   : 다운로드 사이트에 가서 
   : jdk-8u291-linux-x64.tar.gz 다운로드 한다.(Java8)
   wget jdk-8u291-linux-x64.tar.gz
    
####2. linux 서버(root 홈디렉토리)에 업로드 하기
   : 작업 디렉토리는 /root (root 홈)

####3. 압축을 푼다.
   "# tar xvfz jdk-8u291-linux-x64.tar.gz

####4. 더존 소프트웨어 설치 디렉토리 만들기
   "# mkdir /usr/local/douzone

####5. 설치
   "# mv jdk1.8.0_291 /usr/local/douzone/java1.8

####6. 링크 파일 생성
   "# ln -s /usr/local/douzone2021/java1.8 /usr/local/douzone/java
![자바링크드파일 만든후](https://user-images.githubusercontent.com/90162940/135235137-b2126d80-ad84-4261-8689-e8e1867e8ef1.PNG)



####7. 설정(/etc/profile)

"# java
export JAVA_HOME=/usr/local/douzone2021/java
export CLASSPATH=$JAVA_HOME/lib/tools.jar
export PATH=$PATH:$JAVA_HOME/bin

####8. 현재 shell 환경에 적용하기
 "# source /etc/profile

9. 확인 작업
"# java -version

java version "1.8.0_291"
Java(TM) SE Runtime Environment (build 1.8.0_291-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.291-b10, mixed mode)


