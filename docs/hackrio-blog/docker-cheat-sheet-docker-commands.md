# Docker 备忘单(Docker 命令+免费 PDF)

> 原文：<https://hackr.io/blog/docker-cheat-sheet-docker-commands>

Docker 是一个开源的容器化平台，用于在服务器和云上构建、运行和管理容器。它是创建和管理容器化应用程序的事实标准。Docker 作为编排容器的行业标准于 2013 年推出。

容器是一个软件单元，它结合了应用程序的源代码和操作系统库(T2)以及依赖关系，因此应用程序可以在任何环境下工作。

今天，大多数公司使用 Docker 来管理和交付具有复杂需求的分布式应用程序。所以，对码头工人专家的需求也在以惊人的速度增长。

所以，如果你想涉足这个领域，你必须准备好应对面试的所有技术材料。我们创建了这个 Docker 命令备忘单，让您的生活更轻松。你可以参考这个 Docker 备忘单来复习你的知识。

## **为什么是 Docker？**

以前，开发人员创建具有多种依赖关系的复杂应用程序，并根据底层基础设施管理它们的运行时，是一件非常具有挑战性的事情。但是有了 Docker ，开发人员可以简单地将复杂的应用程序分解成更小的部分，将它们与运行该容器所需的所有依赖文件一起放入容器中，而与底层基础设施无关。

开发者可以在任何安装了 Docker 运行时的 OS 兼容主机(Linux 或 Windows)上快速运行 Docker 容器。

以下是 码头工人 的一些显著特征:

*   Docker 支持微服务架构。
*   便利的封装、隔离、可移植性和控制。
*   Docker 容器很小(兆字节)。它们带有版本控制和组件重用的内置机制。
*   Docker 允许你有效地利用所有容器中的资源。
*   它允许开发人员快速行动，提高开发和部署速度，以交付高端软件。
*   使用 Docker，您可以轻松地使您的应用程序可移植，并可以在不同的基础设施上共享它来运行容器。

信不信由你，通过消除对底层基础架构的依赖，多家公司已经从中受益，加快了 SDLC 流程并提高了性能。

## **Docker 的先决条件**

以下是不同操作系统安装 docker 的一些主要前提:

3.10 . x 内核是 Docker 的最低要求。

需要 10.8“山狮”或更新版本。

必须在 BIOS 中启用 Hyper-V。

如果可用，还必须启用 VT-D(英特尔处理器)。

您应该将 Windows Server 2016 作为安装 docker 和 docker-compose 的最低版本。这个版本有一些限制，比如多个虚拟网络和 Linux 容器。建议使用 Windows Server 2019 及更高版本，以获得更好的兼容性。

## **安装对接器**

要在您的系统上安装 docker，您可以从系统的命令行终端执行简单的命令，如下所示。如果下面没有提到您的具体操作系统步骤，您可以在线了解。

运行下面的命令是在 Linux 操作系统上快速安装 Docker 的最简单的方法。

```
curl -sSL https://get.docker.com/ | sh
```

下载并安装 Docker 社区版。对于家酿木桶，只需将酿造桶安装在码头上。或者你可以下载并安装 Docker 工具箱。苹果电脑

安装 Docker Community Edition 后，点击 Launchpad 中的 Docker 图标启动一个容器。

```
docker run hello-world
```

可以安装 [Docker for Windows 10](https://docs.docker.com/desktop/windows/install/) 。安装完成后，双击 Docker 安装程序运行。完成安装过程后，转到指示 Docker 正在运行的通知中的鲸鱼图标，您可以通过终端访问它。 Windows 10

您可以从终端运行以下命令来检查安装的 Docker 版本。

```
docker version
```

借助 OneGet 提供商 PowerShell 模块，您可以轻松地在 Windows Server 上安装 Docker EE。首先，您需要从 PowerShell Gallery 安装 Docker-Microsoft package management 提供程序模块。

```
Install-Module -Name DockerMsftProvider -Repository PSGallery -Force
```

要查看已安装的软件包提供程序和 Docker 软件包，请键入以下命令:

```
Get-PackageProvider -ListAvailableget-packagesource -ProviderName DockerMsftProvider
```

要安装最新版本的 Docker，请使用以下命令

```
Install-Package -Name docker -ProviderName DockerMsftProvider
```

要检查已安装的 Docker 版本，请运行以下命令:

## **Docker 的架构**

DevOps 架构有五大工作实体，分别是注册表、镜像、容器、守护进程、客户端。

*   **注册中心** :它托管 Docker 图像，包括公共图像和官方图像。Docker Hub 是每个人都使用的默认 Docker 注册表。
*   **Image** :你可以在启动一个容器的时候直接或者隐式的从注册表中下载 Docker 镜像。
*   **容器** :是一个图像的实例。单个图像有几个可用的容器。
*   Docker 守护进程 :守护进程执行主要任务，比如创建、运行和监控容器，以及构建和存储映像。
*   **客户端** :客户端借助 HTTP 与 Docker 守护进程通信。

现在，让我们从 Docker 命令列表开始。我们将首先介绍上面提到的 Docker 体系结构的五个实体的 Docker 命令。

## **Docker 命令备忘单**

**[下载备忘单](https://drive.google.com/file/d/1JCm0GKQkTOsuDW4jOStkeHVJZ1AkhMPT/view?usp=sharing)**

### **注册处&存储库**

存储库是指为容器创建文件系统的映像的托管集合。Registry 是指包含存储库并提供帮助管理存储库的 HTTP API 的主机。

Docker 有一个包含数千个存储库的中央注册中心。但是在使用这个注册表中的图像之前，请确保验证它们以避免安全问题。

*   **docker 登录** :登录注册表。
*   **docker logout** :从注册表中注销。
*   **docker 搜索** :它会在注册表中搜索图片。
*   **docker pull** :它将从注册表中提取一个图像到本地机器。
*   **docker push**: It will push an image to the registry from the local machine.

    **图像**

### 您可以将图像作为 Docker 容器的模板。您可以运行以下命令来处理图像:

**docker 图片:** 它会显示所有图片。

*   **docker 导入:** 你可以从一个 tarball 创建一个图像。
*   **docker build:** 你可以从 Dockerfile 创建一个镜像。
*   **docker commit:** 你可以从一个容器中创建一个映像，如果它正在运行，可以暂时暂停它。
*   **docker rmi:** 它会移除一个图像。
*   **docker load** :它将从一个 tar 文档中加载一个图像作为 STDIN，包括图像和标签。
*   **docker:** 它会将一个图像保存到一个 tar 存档流中，并输出所有的父层、标签、&版本。
*   **docker 历史** :显示图像的历史
*   **docker tag** :它会给图片贴上一个名字标签。
*   **docker load<my _ image . tar . gz**:它会从所提到的文件中加载一张图片，并附上它的历史记录。
*   **docker save my _ image:my _ tag | gzip>my _ image . tar . gz**:它会保存一个已经存在的文件。
*   **cat my _ container . tar . gz | docker import-my _ image:my _ tag**:它会从提到的文件中导入容器作为图像，而不包含它的历史；因此，文件很小。
*   **docker export my _ container | gzip>my _ container . tar . gz**:会导出容器。
*   **docker push repo[:tag]** :它将从注册表中推送一个映像或 repo。
*   **docker pull repo[:tag]:**它会从注册表中拉出一个映像或 repo。
*   **集装箱**
*   **docker search text:** It will allow you to search for an image in the official registry.

    容器是包含要执行的代码的独立 Docker 进程。

### **docker create:** 它会创建一个容器而不启动它。

**码头工人重命名** :重新制造集装箱。

*   **docker run** :它会在一个任务中创建并启动容器。
*   **docker rm:** 它会删除一个容器。
*   **docker 更新** :它将更新一个容器的资源限制。
*   通常，如果你在没有任何选项的情况下运行容器，它会立即启动和停止。
*   **docker run-TD container _ id**:它会保持容器运行，-t 会分配一个伪 TTY 会话，-d 会自动分离容器。

**docker run - rm** :一旦停止就会把集装箱移走。

*   **docker run-v $ HOSTDIR:$ docker dir**:将主机上的一个目录映射到 docker 容器。
*   **docker rm -v** :它将删除与容器相关联的卷。
*   **Docker run-log-driver = syslog**
*   **docker start** :它会启动一个容器，所以它在运行。
*   **docker stop** :停止正在运行的集装箱。
*   **docker restart** :停止并启动一个集装箱。
*   **docker pause:** 它会暂停一个正在运行的容器，把它“冻结”在原地。
*   **docker unpause** :将一个运行中的容器解包。
*   **docker wait** :它会一直阻塞，直到正在运行的集装箱停止。
*   **docker kill** :它向一个正在运行的容器发送一个 SIGKILL。
*   **docker attach** :它将连接到一个正在运行的容器。
*   docker run-It-c 512 agile ek/CPU set-test:它让你限制 CPU，要么使用所有 CPU 的百分比，要么使用特定的核心。1024 意味着 100%的 CPU，因此如果您希望容器占用所有 CPU 核心的 50%，您应该指定 512。
*   **docker run-it-cpuset-CPU = 0，4，6 agileek/cpuset-test** :使用 cpuset-CPU 的 CPU 核心。
*   **docker run-it-m 300m Ubuntu:14.04/bin/bash**:对 Docker 设置内存约束。
*   **docker run-RM-it-cap-add SYS _ ADMIN-device/dev/fuse sshfs**:使用 cap-add 设置 Linux 功能。它允许您挂载基于 FUSE 的文件系统，并且您需要将-- cap-add 和-- device 结合起来
*   docker run-it-device =/dev/ttyusb 0 debian bash:提供对单个设备的访问。
*   docker run-it-privileged-v/dev/bus/USB:/dev/bus/USB debian bash:提供对所有设备的访问。
*   **docker ps** :显示正在运行的集装箱。
*   **docker 日志** :提供容器中的日志。(您可以使用定制的日志驱动程序，但是在 1.10 中，日志只适用于 json-file 和 journald)。
*   **docker inspect** :检查一个集装箱的所有信息(包括 IP 地址)。
*   **docker 事件** :从容器中获取事件。
*   **docker port** :显示集装箱面向公众的港口。
*   **docker top:** 它会显示容器中正在运行的进程。
*   **docker stats** :显示容器的资源使用统计。
*   **docker diff:** 它会显示容器的 FS 中发生变化的文件。
*   **docker ps -a** :显示正在运行和停止的集装箱。
*   **docker stats - all** :会显示所有容器的列表，默认显示刚刚运行。
*   docker cp :它会在容器和本地文件系统之间复制文件或文件夹。
*   docker export :它将把容器文件系统转换成一个 tarball 归档流输出到 STDOUT。
*   **docker exec** :执行一个容器中的命令。
*   **docker exec-it foo/bin/bash**:要进入一个正在运行的容器，在一个名为 foo 的正在运行的容器上附加一个新的 shell 进程。

*   **Dockerfile 备忘单**
*   **docker commit container image:** It will commit a new docker image.

    这是一个配置文件，当你运行 docker 构建时，它将建立一个 Docker 容器。要创建 docker 文件，您可以使用以下任何文本编辑器及其语法突出显示模块。

### 崇高文字 2

Atom

*   Vim
*   Emacs
*   文字
*   VS 代码
*   以下是您在使用 Dockerfile 时可以使用的一些说明:
*   起**:为后续指令设置基础图像。**

**MAINTAINER** (已弃用——用标签代替):它将设置生成图像的作者字段。

*   **运行** :它将在当前图像之上的新图层中执行任何命令，然后提交结果。
*   **CMD** :提供执行容器的默认值。
*   **EXPOSE** :它会告诉 Docker 容器在运行时监听指定的网络端口。
*   **添加** :将新文件、目录或远程文件复制到容器中。
*   **复制** :将新的文件或目录复制到一个容器中。默认情况下，无论用户/WORKDIR 设置如何，它都会以 root 用户身份进行复制。使用- chown= <用户> : <组>将所有权提供给另一个用户/组。
*   **入口点** :它将配置一个作为可执行文件运行的容器。
*   **VOLUME** :为外部挂载的卷或其他容器创建一个挂载点。
*   **用户** :为后面的 RUN / CMD / ENTRYPOINT 命令设置用户名。
*   **工作目录** :设置工作目录。
*   **ARG** :它让你定义一个构建时变量。
*   **网络**
*   Docker 有一个特色网络，允许容器连接。您可以使用 Docker 创建三个网络接口，即网桥、主机和无。
*   **ONBUILD**: It will add a trigger instruction when the image is used as the base for another build.

    默认情况下，新容器被发送到桥接网络中。为了在几个容器之间建立通信，您需要一个新的网络来启动其中的容器。它让容器在与未连接到网络的其他容器隔离的同时进行通信。

### **docker 网络创建名称** :默认情况下会创建一个新的网桥类型的网络。

**docker network rm NAME** :它将删除一个或多个由 NAME 指定的网络，并确保没有容器连接到被删除的网络。

**docker network ls** :会列出所有的网络。

*   **docker 网络监控名称** :显示一个或多个网络的详细信息。
*   **docker 网络连接网络容器** :将容器连接到网络
*   **卷**
*   Docker 的卷是自由浮动的文件系统。因此不需要连接到特定的容器。为了便于携带，您可以使用从纯数据容器装载的卷。根据 Docker 1.9.0，它带有命名卷，取代了纯数据容器。
*   **docker 卷创建** :创建卷。
*   **docker network disconnect NETWORK CONTAINER**: It will disconnect a container from a network.

    **docker 卷 rm** :移除卷。

### **docker 卷 ls** :列出卷。

**编排**

*   编排管理容器的生命周期，尤其是在动态环境中。您可以使用它来控制和自动化容器的几个任务。
*   在一长串 Docker 编排工具中，最常用的编排工具是 Docker Swarm、Kubernetes 和 Mesos。在这个 Docker 备忘单中，我们使用了 Docker Swarm 命令。
*   **Docker swarm init-advertise-addr 10 . 1 . 0 . 2**:初始化 swarm 模式，监听特定接口。
*   **docker volume inspect**: To inspect the volumes.

    **Docker swarm join-token<manager-token>10 . 1 . 0 . 2:2377**:它将作为管理节点加入一个已有的 swarm。

### **Docker swarm join-token<worker-token>10 . 1 . 0 . 2:2377**:它将作为一个工作者节点加入一个 swarm。

**Docker node ls** :会列出群中的所有节点。

**Docker service create-replicas 3-p 80:80 name-webn gix**:它将从现有端口上的映像创建一个服务，并部署三个实例。

*   **Docker service ls** :它会列出成群运行的服务。
*   Docker service scale web=5 :它会对服务进行缩放。

*   **与容器的交互**
*   你可以使用以下命令与容器交互。
*   **Docker exe-ti container _ name command . sh**:它会在容器中运行一个命令。
*   **Docker logs -ft 集装箱名称** :跟随集装箱日志。
*   **docker service ps web**: It will list the tasks of service.

    **建造**

### 您可以使用以下命令从 Docker 文件构建图像。

Docker build-t myapp:1.0-将从 Docker 文件构建一个图像并标记它。

*   **Docker images** -它将列出所有本地存储的图像
*   **Docker RMI alpine:3.4**会从 Docker 存储中删除一张图片。
*   **Docker commit -m “commit message” -a “author” container_name username/image_name: tag**: It will save the running container as an image.

    [Docker&Kubernetes:实用指南【2023 版】](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.3490000&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fdocker-kubernetes-the-practical-guide%2F)

### **清理**

为了优化资源的使用，您需要经常清理资源以保持性能。您可以运行以下命令来清理资源。

*   **Docker 图像修剪** :它将清理一个未使用的/悬空的图像
*   **Docker image prune -a** :它将删除一个没有在容器中使用的图像。
*   Docker 系统修剪 :它会修剪整个系统。

**Docker 蜂群离开** :它会离开蜂群。

### **docker stack RM stack _ name**:会移除一个蜂群。

**Docker 杀$ (docker ps -q)** :会 v.

*   **docker RM $(docker PS-a-q)**:将删除所有停止的集装箱
*   **服务**
*   现在让我们先睹为快，看看用于查看正在运行的服务、运行服务、查看所有服务日志以及扩展服务的命令。
*   **Docker service ls** :它会列出一个群中运行的所有服务。
*   **Docker stack services stack _ name**:显示所有正在运行的服务。
*   **Docker 服务日志 stack_name service_names** :显示所有服务日志。

*   **docker rmi $(docker images -q)**: It will delete all images.

    **坞站-合成 Cheat Sheet**

### Compose 是一个帮助你定义和运行多容器 Docker 应用程序的工具。使用 Compose，您可以使用 YAML 文件来配置应用程序服务。在以下命令的帮助下，您可以从您的配置中简单地创建和启动所有服务。

**docker-compose start** :将启动容器。

*   **docker-compose stop** :停止集装箱。
*   **docker-compose pause** :会暂停容器。
*   **docker-compose un pause**:将容器解包。
*   **Docker service scale stack_name_service_name= replicas**: It will scale a service across qualified nodes.

    **docker-compose ps** :会列出所有的容器。

### **docker-compose up** :它聚合每个容器的输出(本质上是运行 docker-compose logs - follow)。

**Docker-compose down** :它停止容器并删除由 up 创建的容器、网络、卷和映像。

*   **Docker-compose-f<Docker-compose-file>up**:它将启动你的应用
*   **docker-compose stop-使用-d 标志在分离模式下运行 docker-compose** ，然后你可以在任何需要的时候停止它。
*   **基本示例**
*   [Docker 认证助理:2023 年硕士课程](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.2074534&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fdocker-certified-associate%2F)
*   **结论**
*   Docker 是一款提供平台即服务服务的软件，通过将软件封装在容器中来创建和部署应用程序。
*   容器是轻量级的、可移植的实体，可以很容易地被共享，而不需要依赖底层的基础设施或者担心它们与几个系统的兼容性。由于 docker 容器的特性，许多公司现在都采用它来创建复杂的应用程序。
*   Docker 附带了一系列与其服务相关的术语，例如 Docker 文件、图像、容器和其他 Docker 特有的词汇。一切都可以使用 Docker 命令来处理。在这个 [**Docker 备忘单 PDF**](https://drive.google.com/file/d/1JCm0GKQkTOsuDW4jOStkeHVJZ1AkhMPT/view?usp=sharing) **，** 中，你会得到一个你可以随时查阅的所有 Docker 命令的列表。
*   **码头工人常见问题解答**

### **Docker 命令都是什么？**

```
# docker-compose.yml

version: '2'

services:

  web:

    build: .

    # build from Dockerfile

    context: ./Path

    dockerfile: Dockerfile

    ports:

     - "5000:5000"

    volumes:

     - .:/code

  redis:

    image: redis
```

```
Building

web:

  # build using the Dockerfile

  build: .

 # build using the custom Dockerfile

  build:

    context: ./dir

    dockerfile: Dockerfile.dev

 # build from image

  image: ubuntu

  image: ubuntu:14.04

  image: tutum/influxdb

  image: example-registry:4000/postgresql

  image: a4bc65fd
```

```
 ports:

    - "3000"

    - "8000:80"  # guest:host

 # expose ports to linked services (not to host)

  expose: ["3000"]

Commands

 # commands to execute

  command: bundle exec thin -p 3000

  command: [bundle, exec, thin, -p, 3000]

 # overriding the entrypoint

  entrypoint: /app/start.sh

  entrypoint: [php, -d, vendor/bin/phpunit]
```

```
# environment variables

  environment:

    RACK_ENV: development

  environment:

    - RACK_ENV=development

 # environment vars from the specified file

  env_file: .env

  env_file: [.env, .development.env]
```

```
 # makes the `db` service available as the hostname `database`

  # (implies depends_on)

  links:

    - db:database

    - redis

 # make sure `db` is alive before starting

  depends_on:

    - db
```

```
# make this service extend another

  extends:

    file: common.yml  # optional

    service: web app

 volumes:

    - /var/lib/mysql

    - ./_data:/var/lib/mysql
```

**Docker 命令都是什么？**

## 你可以点击这里下载我们的 Docker 命令备忘单 PDF。

### **docker 中的 ENV 命令是什么？**

**docker 中的 ENV 命令是什么？**

您可以使用 ENV 为容器中未来的环境变量提供默认值。您不能通过命令行更改 ENV 变量，但是如果您愿意，可以使用 ARG 变量。

## 在下面 Dockerfile 的例子中，我们创建了两个变量，一个作为 ARG，一个作为 ENV。

*   **使用环境变量**中的参数值

【Dockerfile 需要 CMD 吗？

*   CMD 指令允许开发者设置一个默认命令，只有在运行一个容器而没有指定命令时才会执行。如果您使用命令运行 Docker 容器，它将忽略默认命令。如果 Dockerfile 有多个 CMD 指令，所有最后的 CMD 指令都会被忽略。

CMD ["executable "，" param1 "，" param2"] (exec 格式，首选)

CMD ["param1 "，" param2"](为 exec 表单中的入口点设置额外的默认参数)

命令参数 1 参数 2(外壳形式)

```
FROM alpine:3.7
ARG VARIABLE_1=5
ENV VARIABLE_2=$VARIABLE_1
RUN echo "print variable value:" $VARIABLE_1
RUN echo " print ENV variable : " $VARIABLE_2
```

*   ### **如何学习 Docker 命令？**

有几个在线和离线的资源可以让你学习 Docker 命令。为此，您需要对命令行有深入的了解。此外，您可以浏览 Docker 命令备忘单，温习您的技能，以便快速参考。

### **Docker CLI 还免费吗？**

*   Docker CLI 还免费吗？
*   个人/学生/小企业仍可免费享受 Docker。小企业的员工不到 250 人，年营业额不到 1000 万美元。
*   [点击此处](https://www.docker.com/pricing/) 查看完整定价详情。

*   ### **如何执行 docker 容器？**

要执行 docker exec 命令，您必须有一个正在运行的 docker 容器。如果没有，使用下面的 docker run 命令启动一个测试容器:

*   这个命令从官方的 alpine 映像创建一个新的 Docker 容器。

如果你愿意，你可以使用下面的命令重命名你的容器名。

如果你想在 Docker 容器中运行一个交互式 shell，你需要运行带有"-i "(保持容器的输入开放)和"-t "(创建一个 shell 可以连接的伪终端)标志的" docker exec "。

*   它将在指定的容器中运行 sh shell，给出一个基本的 shell 提示符。若要退出容器，请运行以下命令。

*   如果你想在你的容器中以不同的用户身份运行一个命令，运行下面的命令。

```
docker run -d --name container-name alpine watch "date >> /var/log/date.log"
```

为了将环境变量和要运行的命令一起传递到容器中，可以使用-e 标志，如下所示。

*   为了设置多个变量，对每个变量重复-e 标志。

```
docker ps
```

*   首先，用文本编辑器制作文件。我们将在这里用 nano 打开一个新文件。

```
docker rename container-name new-name
```

*   我们已经使用了。env 作为文件名来管理版本控制之外的信息。

```
docker exec -it container-name sh
```

将您的 KEY=value 变量写入文件，每行一个，如下所示。

```
Exit
```

*   保存并关闭文件。要保存文件并退出 nano，请按 CTRL+O，然后按 ENTER 保存，再按 CTRL+X 退出。

```
docker exec --workdir /tmp container-name pwd
```

*   现在运行 docker exec 命令，在- env-file 之后指定正确的文件名

```
docker exec --user guest container-name whoami
```

```
    docker exec -e TEST=sammy container-name env
    ```

    坞站【exec】env 文件。env 容器名称 env〔t5〕

```
nano .env
```

**人也在读:**

*   Write your KEY=value variables into the file, one per line, like the following.

```
TEST=sammy
ENVIRONMENT=prod
```

*   Save and close the file. To save the file and exit nano, press CTRL+O, then ENTER to save, then CTRL+X to exit.
*   Now run the docker exec command, specifying the correct filename after --env-file

| docker exec --env-file .env container-name env |

**People are also reading:**