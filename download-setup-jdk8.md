1. Download Oracle JDK8 
link : https://www.oracle.com/java/technologies/downloads/

In console :

2. cd Downloads

4. sudo mkdir /usr/lib/jvm

5. cd /usr/lib/jvm

6. sudo tar xvzf ~/Downloads/jdk[version].tar.gz

7. sudo nano /etc/environment, after opened with nano or gedit,
and following this command in your tab variable file:
      
## Before 
PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin"

## or Blank !

## After open, following your command in variable file:
                            
/usr/lib/jvm/jdk1.8.0_341/bin
/usr/lib/jvm/jdk1.8.0_341/jre/bin

J2SDKDIR="/usr/lib/jvm/jdk1.8.0_341"
J2REDIR="/usr/lib/jvm/jdk1.8.0_341/jre"
JAVA_HOME="/usr/lib/jvm/jdk1.8.0_341"
JRE_HOME="/usr/lib/jvm/jdk1.8.0_341/jre/bin"

PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/>
PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/>
J2SDKDIR="/usr/lib/jvm/jdk1.8.0_341"
J2REDIR="/usr/lib/jvm/jdk1.8.0_341/jre"
JAVA_HOME="/usr/lib/jvm/jdk1.8.0_341"
JRE_HOME="/usr/lib/jvm/jdk1.8.0_341/jre/bin"

save and close with Ctrl + x + Y [enter]

8. and then,  enter command in your terminal and following

sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_341/bin/java" 0

sudo update-alternatives --install "/usr/bin/javac" "javac" "/usr/lib/jvm/jdk1.8.0_341/bin/javac" 0

sudo update-alternatives --set java /usr/lib/jvm/jdk1.8.0_341/bin/java

sudo update-alternatives --set javac /usr/lib/jvm/jdk1.8.0_341/bin/javac

9. ## Verify the setup

update-alternatives --list java
output > /usr/lib/jvm/jdk1.8.0_341/bin/java

update-alternatives --list javac
output > /usr/lib/jvm/jdk1.8.0_341/bin/javac

10. Check Java Version with command 
java -version 
output > ava version "1.8.0_341"
Java(TM) SE Runtime Environment (build 1.8.0_341-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.341-b10, mixed mode)
