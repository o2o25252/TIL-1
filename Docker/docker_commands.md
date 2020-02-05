# Docker Commands
도커의 명령어 모음


**Basic Commands Sytax**
```bash
docker <option> <command> <ARG...>
```
* option | 옵션
* command | 명령
* ARG... | 매개변수

> 링크를 클릭하여 이동  
| [attach](#attach) | [build](#build) | [commit](#commit) | [cp](#cp) | [create](#create) | [diff](#diff) |  [events](#events) | [exec](#exec) | [export](#export) | [history](#history) | [images](#images) | [import](#import) | [info](#info) | [inpect](#inspect) | [kill](#kill) | [load](#load) | [login](#login) | [logout](#logout) | [logs](#logs) | [pause](#pause) | [port](#port) | [ps](#ps) | [pull](#pull) | [push](#push) | [rename](#rename) | [restart](#restart) | [rm](#rm) | [rmi](#rmi) | [run](#run) | [save](#save) | [search](#search) | [start](#start) | [stats](#stats) | [stop](#stop) | [tag](#tag) | [top](#top) | [unpause](#unpause) | [update](#update) | [version](#version) | [wait](#wait) |


## attach
>Attach local standard input, output, and error streams to a running container.  
실행되고 있는 컨테이너에 입력(<code>stdin</code>)과 출력(<code>stdout</code>)을 연결하는 명령어.  

  * **Syntax**
  ```bash
  docker attach <option> <containerName, ID>
  ```

## build
> Build an image from a Dockerfile  
Dockerfile로 image를 생성하는 명령어.

 * **syntax**
  ```bash
  docker build <option> <dockerfile Path>
  ```

* Local path 와 URL 사용 가능
* Dockerfile 이 있는 경로에서 build 명령을 실행

## commit
> Create a new image from a container's changes.  
컨테이너의 변경 사항을 이미지로 생성하는 명령어.

  * **Syntax**
  ```bash
  docker commit <option> <containerName, ID> <repositoryName>/<imageName>:<tag>
  ```


## cp
> Copy files/folders between a container and the local filesystem.  
컨테이너의 Directory/files을 host로 복사하는 명령어.

  * **Syntax**
  ```bash
  docekr cp <containerName>:<path> <hostPath>
  ```

## create
> Create a new container.  
Image로 컨테이너를 생성하는 명령어.

  * **Syntax** 
  ```bash
  docker create <option> <imageName, ID> <command> <ARG...>
  ```

## diff
> Inspect changes to files or directories on a container's filesystem.  
컨테이너에서 변경된 file을 확인하는 명령어.  

  * **Syntax**  
  ```bash
  docker diff <containerName, ID>
  ```

  * 변경된 파일 비교 기준 --> 컨테이너를 생성한 이미지의 내용

## events
> Get real time events from the server.  
Docker 서버에 일어난 event를 실시간으로 출력하는 명령어.

  * **Syntax**  
  ```bash
  docker events
  ```

  * 해당 명령어를 실행하게 되면 docker는 대기 상태가 된다.

## exec
> Run a command in a running container.  
외부에서 컨테이너 안의 명령을 실행하는 명령어.  

  * **Syntax**  
  ```bash
  docker export <option> <containerName, ID> <command> <ARG...>
  ```  

## export
> Export a container's filesystem as a tar archive.  
컨태이너의 filesystem을 tar 파일로 저장하는 명령어.  

  * **Syntax**  
  ```bash
  docker export <containerName, ID>
  ```

  * 컨테이너의 내용이 표준 출력으로 출력된다.

## history
> Show the history of an image.  
Image의 history를 출력하는 명령어.

  * **Syntax**
  ```bash
  docker history <option> <imageName, ID>
  ```

## images
> List images.  
Image의 목록을 출력하는 명령어.

  * **Syntax**
  ```bash
  docker images <option> <imageName>
  ```

## import
> Import the contents from a tarball to create a filesystem image.  
tar file로 압축된 filesystem으로부터 image를 생성하는 명령어.

  * **Syntax**  
  ```bash
  docker import <tar file's URL or-> <repositoryName>/<imageName>:<tag>
  ```

## info
> Display system-wide information.  
시스템, Docker Container, Image rotn, setting 등의 info를 출력하는 명령어.

 * **Syntax**
 ```bash
 docker info
 ```

## inspect
> Return low-level information on Docker objects.  
container, image의 세부 정보를 JSON 형태로 출력하는 명령어.  

  * **Syntax**
  ```bash
  docker inspect <option> <containerName of imageName, ID>
  ```

## kill
> Kill one or more running containers.  
컨테이너를 중지하는 명령어.  

  * **Syntax**
  ```bash
  docker kill <option> <containerName, ID>
  ```

## load
> Load an image from a tar archive or STDIN.  
tar file로 image를 생성하는 명령어.  

  * **Syntax**
  ```bash
  docker load <option>
  ```

  * tar file은 image 이름과 태그가 포함되어 있다.

## login
> Log in to a Docker registry.  
Docker 레지스트리에 로그인 하는 명령어.  

  * **Syntax**
  ```bash
  docker login <option> <dockerRegistryURL>
  ```

## logout
> Log out from a Docker registry.  
Docker 레지스트리에서 로그아웃 하는 명령어.  

  * **Syntax**
  ```bash
  docker logout <dockerRegistryServerURL>
  ```

## logs
> Fetch the logs of a container.  
컨테이너의 log를 출력하는 명령어.  

  * **Syntax**
  ```bash
  docker logs <containerName, ID>
  ```

## pause
> Pause all processes within one or more containers.  
컨테이너에서 실행되고 있는 모든 processes를 일시 정지하는 명령어.  

  * **Syntax**
  ```bash
  docker pause <containerName, ID>
  ```

## port
> List port mappings or a specific mapping for the container.  
컨테이너에서 port가 열려 있는지 확인하는 명령어.  

  * **Syntax**
  ```bash
  docker port <containerName, ID> <port>
  ```

## ps
> List containers.  
컨테이너의 목록을 출력하는 명령어.  

  * **Syntax**
  ```bash
  docker ps <option>
  ```

## pull
> Pull an image or a repository from a registry.  
Docker 레지스트리에서 image를 pull받는 명령어.  

  * **Syntax**
  ```bash
  docker pull <option> <repositoryName>/<imageName>:<tag>
  ```

  * \<repositoryName>
    * Docker Hub User Name
    * Repository Address
  * tag를 지정해주지 않으면 tag가 붙은 image가 모두 pull 되버린다.

## push
> Push an image or a repository to a registry.  
Docker 레지스트리에 image를 올리는 명령어.  

  * **Syntax**
  ```bash
  docker push <repositoryName>/<imageName>:<tag>
  ```

  * \<repositoryName>
    * Docker Hub User Name
    * Repository Address
  * tag를 지정해주지 않으면 tag가 붙은 image가 모두 push 되버린다.

## rename
Rename a container

## restart
Restart one or more containers

## rm
Remove one or more containers

## rmi
Remove one or more images

## run
Run a command in a new container

## save
Save one or more images to a tar archive (streamed to STDOUT by default)

## search
Search the Docker Hub for images

## start
Start one or more stopped containers

## stats
Display a live stream of container(s) resource usage statistics

## stop
Stop one or more running containers

## tag
Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE

## top
Display the running processes of a container

## unpause
Unpause all processes within one or more containers

## update
Update configuration of one or more containers

## version
Show the Docker version information

## wait
Block until one or more containers stop, then print their exit codes