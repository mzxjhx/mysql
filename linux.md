## linux学习

### linux目录

### linux环境变量配置

#### Linux环境变量配置方法一：export PATH
如redis安装路径/usr/local/redis-6.0.5
```shell
export PATH=$PATH:/usr/local/redis-6.0.5/src
任意目录输入redis启动命令redis-cli，进入redis
127.0.0.1:6379>
```
* 生效时间：立即生效
* 生效期限：当前终端有效，窗口关闭后无效
* 生效范围：仅对当前用户有效

#### Linux环境变量配置方法二：vim ~/.bashrc
```shell
vim ~/.bashrc
# 在最后一行加上
export PATH=$PATH:/usr/local/redis-6.0.5/src
```
* 生效时间：使用相同的用户打开新的终端时生效，或者手动source ~/.bashrc生效
* 生效期限：永久有效
* 生效范围：仅对当前用户有效

#### Linux环境变量配置方法四：vim /etc/bashrc
```shell
vim /etc/profile

# 在最后一行加上
export PATH=$PATH:/usr/local/redis-6.0.5/src
```

#### Linux环境变量配置方法五：vim /etc/profile 安装jdk1.8
```shell
    export JAVA_HOME=jdk路径
    export JRE_HOME=jdk路径/jre
    export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
    export PATH=${PATH}:${JAVA_HOME}/bin:${JRE_HOME}/bin
    
    //wq退出保存
    source /etc/profile
```

#### 查看Linux环境变量
```shell
    export $PATH
    echo $PATH
```


