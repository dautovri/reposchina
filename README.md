# Repositories in China
How to config the python and scala mirrors

## Tsinghua University mirrors (Ubuntu, Fedora, Arch, Debian)

https://mirrors.tuna.tsinghua.edu.cn/


### Python
#### pip 
``` pip install -i https://pypi.tuna.tsinghua.edu.cn/simple some-package ```

#### conda
```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
```

### Docker 

Add docker mirror
```
docker --registry-mirror=https://registry.docker-cn.com daemon
```

### Maven (Java, Scala)

Alibaba repo 
```http://maven.aliyun.com/nexus/content/groups/public/```


```
<repositories>
        <repository>
            <id>aliyun</id>
            <url>http://maven.aliyun.com/nexus/content/groups/public</url>
        </repository>
</repositories>
```

~/.sbt/repositories

```
[repositories]
local
aliyun: http://maven.aliyun.com/nexus/content/groups/public/
typesafe: http://repo.typesafe.com/typesafe/ivy-releases/, [organization]/[module]/(scala_[scalaVersion]/)(sbt_[sbtVersion]/)[revision]/[type]s/[artifact](-[classifier]).[ext], bootOnly
sonatype-oss-releases
maven-central
sonatype-oss-snapshots
```

More mirrors 

* Alibaba：http://mirrors.aliyun.com/
* NetEase：http://mirrors.163.com/
* Sohu：http://mirrors.sohu.com/
* Xiamen University: http://mirrors.xmu.edu.cn/
* Shanghai Jiaotong University: http://ftp.sjtu.edu.cn/
* University of Science and Technology of China: http://mirrors.ustc.edu.cn/
* Northeastern University: http://mirror.neu.edu.cn/
* Zhejiang University: http://mirrors.zju.edu.cn/
* Neusoft Institute of Information: http://mirrors.neusoft.edu.cn/
