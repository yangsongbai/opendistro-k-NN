
## centos 下构建  
docker pull centos:centos7.3.1611

```
    1  ls -lh
    2  mkdir yangsongbai
    3  cd yangsongbai/
    4  ll
    5  git clone https://github.com/yangsongbai/opendistro-k-NN.git
    6  yum install git 
    7  git clone https://github.com/yangsongbai/opendistro-k-NN.git
    8  cd opendistro-k-NN/
    9  git checkout 7.10.2
   10  git checkout v7.10.2
   11  ll
   12  cd jm
   13  cd jni/
   14  make
   15  cmake .
   16  sudo yum install cmake
   17   yum install cmake
   18  cmake .
   19  cmake -G "Unix Makefiles" ..
   20  whereis
   21  whereis cmake
   22  yum install make -y
   23  cmake .
   25  ll /yangsongbai/opendistro-k-NN/jni/external/
   26  ll /yangsongbai/opendistro-k-NN/jni/external/nmslib/
   27  一git clone https://github.com/nmslib/nmslib.git
   28  git clone https://github.com/nmslib/nmslib.git
   29  cmake .
   30  yum install gcc-c++ -y
   31  cmake .
   32  yum install gcc
   33  yum install gc
   34  cmake .
   35  ll
   36  rm -rf nmslib
   37  rm -rf external/nmslib
   38  cmake .
   39  add_subdirectory given source
   40  cmake . add_subdirectory given source
   41  cmake . add_subdirectory given source
   42  cmake .
   43  tail -100 /yangsongbai/opendistro-k-NN/jni/CMakeFiles/CMakeError.lo
   44  tail -100 /yangsongbai/opendistro-k-NN/jni/CMakeFiles/CMakeError.log
   45  ll
   46  rm -rf  CMakeCache.txt  CPackConfig.cmake CPackSourceConfig.cmake 
   47  ll
   48  rm -rf CMakeFiles
   49  cd ..
   50  git checkout v1.13.0.0
   51  ll
   52  cd jni/
   53  cmake .
   54  ll
   55  cd external
   56  ll
   57  git clone https://github.com/nmslib/nmslib.git
   58  cd ..
   59  ll
   60  cmake .
   61  ake
   62  make
   63  ll
   64  ll release/
   65  make
   66  cmake .
   67  make
   68  cd include/
   69  ll
   70  cat com_amazon_opendistroforelasticsearch_knn_index_v2011_KNNIndex.h 
   71  jdk
   72  java
   73  cd ..
   74  cd ..
   75  cd ..
   76  wget https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
   77  yum install wget 
   78  wget https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
   79  tar -zxf openjdk-13.0.2_linux-x64_bin.tar.gz 
   80  ll
   81  cd jdk-13.0.2/
   82  ll
   83  pwd
   84  vim /etc/profile
   85  yum install vim -y
   86  vim /etc/profile
   87  vim /etc/profile
   88  source /etc/profile
   89  java -version
   90  cd ..
   91  cd opendistro-k-NN/jni/
   92  ll
   93  cmake .
   94  make
```


docker cp dc89b42f6a4c:/yangsongbai/opendistro-k-NN/jni/release/libKNNIndexV2_0_11.so /Users/yangsongbai/workspace/github/opendistro-k-NN/

[docker中宿主机与容器（container）互相拷贝传递文件的方法](https://blog.csdn.net/dongdong9223/article/details/71425077)     

生成的libKNNIndexV2_0_11.so（linux）/libKNNIndexV2_0_11.jnilib(mac) 需要放到es的主目录下   

出现如下报错证明没有安装jdk  
```
In file included from /yangsongbai/opendistro-k-NN/jni/src/com_amazon_opendistroforelasticsearch_knn_index_v2011_KNNIndex.cpp:16:0:
/yangsongbai/opendistro-k-NN/jni/include/com_amazon_opendistroforelasticsearch_knn_index_v2011_KNNIndex.h:2:17: fatal error: jni.h: No such file or directory
 #include <jni.h>
                 ^
compilation terminated.
```