# jenkins_test

第一步：准备jenkins docker 镜像

第二步：配置镜像 https://mirrors.huaweicloud.com/jenkins/update-center.json

第三步：下载插件
            Git
            GitHub
            Pipeline

第四步：创建Job
       配置 GitHub（GitHub项目 + Source Code Management）
       配置构建步骤（Build Steps —— Execute shell）
            pwd
            ls
            go version
            go mod tidy
            go build
            ls

第五步：构建有go环境的jenkins镜像
       Dockerfile
       docker-compose.yml

第六步：开始构建（Build Now）

