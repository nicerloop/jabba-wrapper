# jabba-wrapper

Simple scripts to use jabba (https://github.com/shyiko/jabba) without installation.

Inspired by and tested with maven-wrapper (https://maven.apache.org/wrapper/).

Assembled from jabba install scripts.

## Installation

Simply copy the scripts in the root project folder, keeping the unix shell version executable.

Setup .jabbarc file with the desired JDK version (https://github.com/shyiko/jabba#usage)

Enjoy the wrapper :)

#### macOS / Linux

```sh
curl -sLO https://github.com/nicerloop/jabba-wrapper/raw/master/jabbaw && chmod +x jabbaw
echo "zulu@1.8" > .jabbarc
./jabbaw ./mvnw -v
```

#### Windows 10

```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Invoke-WebRequest -Uri https://github.com/nicerloop/jabba-wrapper/raw/master/jabbaw.ps1 -OutFile ./jabbaw.ps1
"zulu@1.8" | Out-File c:\debug.txt
./jabbaw ./mvnw -v
```