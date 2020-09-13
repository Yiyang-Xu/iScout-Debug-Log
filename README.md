# iScout-编译问题汇总
[TOC]



## Shell 保存日志

![截屏2020-08-30 下午4.50.20](ISout调试笔记.assets/截屏2020-08-30 下午4.50.20.png)

## Git介绍

### master



### branch



#### 用途

- 创建一个属于自己的个人工作分支，以避免对主分支 master 造成太多的干扰，也方便与他人交流协作。
- 当进行高风险的工作时，创建一个试验性的分支，扔掉一个烂摊子总比收拾一个烂摊子好得多。
- 合并别人的工作的时候，最好是创建一个临时的分支，关于如何用临时分支合并别人的工作的技巧，将会在后面讲述。

参考：https://www.raywenderlich.com/675-how-to-use-git-source-control-with-xcode-9#toc-anchor-003

讲的不错

### 用法

#### 创建本地 git Repositories

1.新建项目

2.Source Control --> Create Git Repositories 

<img src="ISout调试笔记.assets/截屏2020-08-28 上午11.08.18.png" alt="截屏2020-08-28 上午11.08.18" style="zoom:25%;" />

3.修改代码

4.Source Control -->commit -->选择文件-->输入备注

<img src="ISout调试笔记.assets/截屏2020-08-28 上午11.06.01.png" alt="截屏2020-08-28 上午11.06.01" style="zoom:50%;" />

5.查看版本，如下

![截屏2020-08-28 上午11.06.39](ISout调试笔记.assets/截屏2020-08-28 上午11.06.39.png)

6.点击可以查看与上一个版本的区别

![截屏2020-08-28 上午11.07.26](ISout调试笔记.assets/截屏2020-08-28 上午11.07.26.png)



#### 提交文件，创建分支

1.修改文件

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.21.20.png" alt="截屏2020-08-30 上午9.21.20" style="zoom:33%;" />

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.53.18.png" alt="截屏2020-08-30 上午9.53.18" style="zoom:50%;" />

A :his is a new file that has not yet been committed to the repository.



2.创建分支，提交文件

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.24.35.png" alt="截屏2020-08-30 上午9.24.35" style="zoom:33%;" />

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.21.02.png" alt="截屏2020-08-30 上午9.21.02" style="zoom:33%;" />

3. 查看版本，master的版本每变，分支延长了，可以创建多个分支

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.23.13.png" alt="截屏2020-08-30 上午9.23.13" style="zoom:25%;" />

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.26.04.png" alt="截屏2020-08-30 上午9.26.04" style="zoom: 25%;" /><img src="ISout调试笔记.assets/截屏2020-08-30 上午9.34.02.png" alt="截屏2020-08-30 上午9.34.02" style="zoom:25%;" />



#### 退回上一个commit的版本 discard all changes

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.57.06.png" alt="截屏2020-08-30 上午9.57.06" style="zoom: 33%;" /><img src="ISout调试笔记.assets/截屏2020-08-30 上午9.57.14.png" alt="截屏2020-08-30 上午9.57.14" style="zoom:33%;" />



<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.57.21-8752705.png" alt="截屏2020-08-30 上午9.57.21" style="zoom:33%;" />

限制在于，只能回退到上一个版本

#### 返回历史版本

点击右上角，分屏

<img src="ISout调试笔记.assets/截屏2020-08-30 上午10.14.32.png" alt="截屏2020-08-30 上午10.14.32" style="zoom:33%;" />

![截屏2020-08-30 上午10.15.14](ISout调试笔记.assets/截屏2020-08-30 上午10.15.14.png)

By default, your current source file is shown on the left and the most recent revision stored in the repository – Git calls this the HEAD – is shown on the right.

查看历史版本

![截屏2020-08-30 上午10.16.27](ISout调试笔记.assets/截屏2020-08-30 上午10.16.27.png)

最开始的版本

![截屏2020-08-30 上午10.17.54](ISout调试笔记.assets/截屏2020-08-30 上午10.17.54.png)

![截屏2020-08-30 上午10.18.52](ISout调试笔记.assets/截屏2020-08-30 上午10.18.52.png)

恢复到该版本，点击中间的箭头，discard change，还可以分区域

![截屏2020-08-30 上午10.20.04](ISout调试笔记.assets/截屏2020-08-30 上午10.20.04.png)

![截屏2020-08-30 上午10.20.54](ISout调试笔记.assets/截屏2020-08-30 上午10.20.54.png)

版本对应

<img src="ISout调试笔记.assets/截屏2020-08-30 上午10.30.44.png" alt="截屏2020-08-30 上午10.30.44" style="zoom:50%;" />

可以显示修改人

<img src="ISout调试笔记.assets/截屏2020-08-30 上午10.32.58.png" alt="截屏2020-08-30 上午10.32.58" style="zoom:50%;" />

#### 切换分支

<img src="ISout调试笔记.assets/截屏2020-08-30 上午10.41.24.png" alt="截屏2020-08-30 上午10.41.24" style="zoom:33%;" />

<img src="ISout调试笔记.assets/截屏2020-08-30 上午10.41.29.png" alt="截屏2020-08-30 上午10.41.29" style="zoom:33%;" /><img src="ISout调试笔记.assets/截屏2020-08-30 上午10.41.52.png" alt="截屏2020-08-30 上午10.41.52" style="zoom:33%;" />

#### 合并分支 Merge

1. 在分支为current下进行修改

2. 修改完后进行commit

3. 将current改为master

4. merge to master

   <img src="ISout调试笔记.assets/截屏2020-08-30 上午10.49.25.png" alt="截屏2020-08-30 上午10.49.25" style="zoom:67%;" />

<img src="ISout调试笔记.assets/截屏2020-08-30 上午10.49.32.png" alt="截屏2020-08-30 上午10.49.32" style="zoom:50%;" />

![截屏2020-08-30 上午10.49.42](ISout调试笔记.assets/截屏2020-08-30 上午10.49.42-8756077.png)

#### 连接到github

参考：https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token

1. 新建项目，可以勾选git,如果没有勾选，后续可以创建（p2）,在方框可以看到新的master

   

   <img src="ISout调试笔记.assets/截屏2020-08-30 上午8.40.04.png" alt="截屏2020-08-30 上午8.40.04" style="zoom:25%;" /><img src="ISout调试笔记.assets/截屏2020-08-30 上午8.42.30.png" alt="截屏2020-08-30 上午8.42.30" style="zoom:25%;" /><img src="ISout调试笔记.assets/截屏2020-08-30 上午8.43.42.png" alt="截屏2020-08-30 上午8.43.42" style="zoom:25%;" />

2. 关联GitHub账号

<img src="ISout调试笔记.assets/截屏2020-08-28 上午9.25.34.png" alt="截屏2020-08-28 上午9.25.34" style="zoom: 33%;" />



3. 点击generate new token ,起名字，然后输入到第二幅图片

![截屏2020-08-28 上午9.29.54](ISout调试笔记.assets/截屏2020-08-28 上午9.29.54.png)

<img src="ISout调试笔记.assets/截屏2020-08-28 上午9.25.42.png" alt="截屏2020-08-28 上午9.25.42" style="zoom:50%;" />

4. 点击新创建的token，打钩赋予权力



![截屏2020-08-30 上午8.34.56](ISout调试笔记.assets/截屏2020-08-30 上午8.34.56.png)

<img src="ISout调试笔记.assets/截屏2020-08-30 上午8.36.49.png" alt="截屏2020-08-30 上午8.36.49" style="zoom:33%;" />

4. 创建github上的repository

<img src="ISout调试笔记.assets/截屏2020-08-30 上午8.45.14.png" alt="截屏2020-08-30 上午8.45.14" style="zoom:33%;" /><img src="ISout调试笔记.assets/截屏2020-08-30 上午8.46.04.png" alt="截屏2020-08-30 上午8.46.04" style="zoom:33%;" />

5.前往GitHub查看

![截屏2020-08-30 上午8.48.58](ISout调试笔记.assets/截屏2020-08-30 上午8.48.58.png)

<img src="ISout调试笔记.assets/截屏2020-08-30 上午8.50.17.png" alt="截屏2020-08-30 上午8.50.17" style="zoom:33%;" />

6. 修改文件，commit 主要是将暂存区里的改动给提交到本地的版本库,修改处有小蓝点

<img src="ISout调试笔记.assets/截屏2020-08-30 上午8.51.13.png" alt="截屏2020-08-30 上午8.51.13" style="zoom:33%;" /><img src="ISout调试笔记.assets/截屏2020-08-30 上午8.50.48-8749846.png" alt="截屏2020-08-30 上午8.50.48" style="zoom:25%;" />

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.11.44-8749937.png" alt="截屏2020-08-30 上午9.11.44" style="zoom:50%;" />

7.查看版本控制

点击first commit 会产生和上一个版本的对比

![截屏2020-08-30 上午9.12.59](ISout调试笔记.assets/截屏2020-08-30 上午9.12.59.png)

<img src="ISout调试笔记.assets/截屏2020-08-30 上午9.14.11.png" alt="截屏2020-08-30 上午9.14.11" style="zoom:50%;" />

#### 查看Github 上的对应分支

<img src="ISout调试笔记.assets/截屏2020-08-30 上午11.07.08.png" alt="截屏2020-08-30 上午11.07.08" style="zoom:33%;" />



#### 从github上获取版本

#### 命令行控制Git

参考：https://blog.csdn.net/denggun12345/article/details/81630547



## 2020.8.28 iSout debug

### Bug1:模拟器适配 

![截屏2020-08-28 下午3.16.40](ISout调试笔记.assets/截屏2020-08-28 下午3.16.40.png)

Building for ios Simulator, but the linked library 'libceres.a' was built for iOS.
iScout.xcodepro

解决方案：file -->projectsettings-->building System -->改为Lagacy Building System



![截屏2020-08-28 下午3.19.45](ISout调试笔记.assets/截屏2020-08-28 下午3.19.45.png)



### Bug2:Boost 库未配置



![截屏2020-08-28 下午4.32.57](ISout调试笔记.assets/截屏2020-08-28 下午4.32.57.png)

'boost/dynamic_bitset.hpp' file not found

#### 安装boost库

方法1：

```bash
brew install boost
```

```bash
Updating Homebrew...
==> Downloading https://mirrors.ustc.edu.cn/homebrew-bottles/bottles/icu4c-64.2.
######################################################################## 100.0%
==> Downloading https://mirrors.ustc.edu.cn/homebrew-bottles/bottles/boost-1.72.
######################################################################## 100.0%
==> Installing dependencies for boost: icu4c
==> Installing boost dependency: icu4c
==> Pouring icu4c-64.2.catalina.bottle.tar.gz
==> Caveats
icu4c is keg-only, which means it was not symlinked into /usr/local,
because macOS provides libicucore.dylib (but nothing else).

If you need to have icu4c first in your PATH run:
  echo 'export PATH="/usr/local/opt/icu4c/bin:$PATH"' >> ~/.zshrc
  echo 'export PATH="/usr/local/opt/icu4c/sbin:$PATH"' >> ~/.zshrc

For compilers to find icu4c you may need to set:
  export LDFLAGS="-L/usr/local/opt/icu4c/lib"
  export CPPFLAGS="-I/usr/local/opt/icu4c/include"

==> Summary
🍺  /usr/local/Cellar/icu4c/64.2: 257 files, 69.3MB
==> Installing boost
==> Pouring boost-1.72.0.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/boost/1.72.0: 14,466 files, 648.6MB
==> Caveats
==> icu4c
icu4c is keg-only, which means it was not symlinked into /usr/local,
because macOS provides libicucore.dylib (but nothing else).

If you need to have icu4c first in your PATH run:
  echo 'export PATH="/usr/local/opt/icu4c/bin:$PATH"' >> ~/.zshrc
  echo 'export PATH="/usr/local/opt/icu4c/sbin:$PATH"' >> ~/.zshrc

For compilers to find icu4c you may need to set:
  export LDFLAGS="-L/usr/local/opt/icu4c/lib"
  export CPPFLAGS="-I/usr/local/opt/icu4c/include"
```

<u>/usr/local/Cellar/boost/1.72.0</u>   这个就是boost 的安装目录



![截屏2020-08-28 下午8.54.52](ISout调试笔记.assets/截屏2020-08-28 下午8.54.52.png)

方法2：似乎是这个成功了

接下来按照这个操作即可

> https://blog.csdn.net/waterbinbin/article/details/62438417?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522159861983519724843339296%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=159861983519724843339296&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v3~pc_rank_v2-1-62438417.first_rank_ecpm_v3_pc_rank_v2&utm_term=Xcode+配置boost&spm=1018.2118.3001.4187



1.配置头文件和链接库

点击项目->TARGETS->Build Settings->Search Pahts->Header Search Paths和Library Search Pahts

添加usr/local/include  以及/usr/local/lib

![img](https://img-blog.csdn.net/20170316203403801?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvd2F0ZXJiaW5iaW4=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)

2.添加需要的libboost_filesystem.a和libboost_system.a文件才能运行成功

点击项目->TARGETS->Build Phases->Link Binary With Libraries

打开/usr/local/lib 找到相应的.a文件拖进去

![img](https://img-blog.csdn.net/20170316203915616?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvd2F0ZXJiaW5iaW4=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)





结果

<img src="ISout调试笔记.assets/截屏2020-08-29 上午9.17.47-8663888.png" alt="截屏2020-08-29 上午9.17.47" style="zoom:50%;" />



### Bug3：开发团队证书过期

Failed to register bundle identifier.

<img src="ISout调试笔记.assets/截屏2020-08-29 上午8.16.20.png" alt="截屏2020-08-29 上午8.16.20" style="zoom:33%;" />

<img src="ISout调试笔记.assets/截屏2020-08-29 上午8.16.24.png" alt="截屏2020-08-29 上午8.16.24" style="zoom:33%;" />

![截屏2020-08-29 上午9.21.00](ISout调试笔记.assets/截屏2020-08-29 上午9.21.00.png)





解决P1：

修改bundle Idetifier

<img src="ISout调试笔记.assets/截屏2020-08-29 上午9.31.29-8665175.png" alt="截屏2020-08-29 上午9.31.29" style="zoom:33%;" />

变为————》

<img src="ISout调试笔记.assets/截屏2020-08-29 上午9.38.18.png" alt="截屏2020-08-29 上午9.38.18" style="zoom:33%;" />



结果

![截屏2020-08-29 上午9.38.08](ISout调试笔记.assets/截屏2020-08-29 上午9.38.08.png)

参考：https://blog.csdn.net/liuzehn/article/details/84142253?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522159866497519725222461316%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=159866497519725222461316&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v3~pc_rank_v2-1-84142253.first_rank_ecpm_v3_pc_rank_v2&utm_term=The+app+identifier+%22com.nizamu&spm=1018.2118.3001.4187

原因讲解：

https://blog.csdn.net/qq_31337641/article/details/78401465?utm_medium=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.channel_param&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.channel_param

### Bug4:Linker command failed with exit code 1 (use -v to see invocation)文件重复

![截屏2020-08-29 上午10.14.58](ISout调试笔记.assets/截屏2020-08-29 上午10.14.58.png)

ld:5  duplicate symbols for architecture x86_64:  ======>>>>这行文字的意思在x86_64平台上编译的时候有5个重复的元素：

报错信息

```
Showing All Errors Only

Ld /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Products/Debug-iphoneos/iScout.app/iScout normal arm64

  cd /Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout

  export PATH="/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/usr/bin:/Applications/Xcode.app/Contents/Developer/usr/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"

  /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/clang++ -Xlinker -rpath -Xlinker /usr/lib/swift -target arm64-apple-ios12.1 -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS13.6.sdk -L/Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Products/Debug-iphoneos -L/Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/VINS_ThirdPartyLib -L/Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/Resources -L/Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/VINS_ThirdPartyLib/ceres-solver/ceres-bin/lib -L/usr/local/lib -F/Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Products/Debug-iphoneos -FVINS_ThirdPartyLib -FVINS_ThirdPartyLib/ceres-solver -FVINS_ThirdPartyLib/eigen3 -FVINS_ThirdPartyLib/ceres-solver/cmake -FVINS_ThirdPartyLib/ceres-solver/config -FVINS_ThirdPartyLib/ceres-solver/include -FVINS_ThirdPartyLib/ceres-solver/internal -FVINS_ThirdPartyLib/ceres-solver/ceres-bin -FVINS_ThirdPartyLib/ceres-solver/docs -FVINS_ThirdPartyLib/ceres-solver/examples -FVINS_ThirdPartyLib/ceres-solver/scripts -FVINS_ThirdPartyLib/ceres-solver/jni -FVINS_ThirdPartyLib/ceres-solver/data -FVINS_ThirdPartyLib/eigen3/unsupported -FVINS_ThirdPartyLib/eigen3/Eigen -FVINS_ThirdPartyLib/ceres-solver/config/ceres -FVINS_ThirdPartyLib/ceres-solver/include/ceres -FVINS_ThirdPartyLib/ceres-solver/internal/ceres -FVINS_ThirdPartyLib/ceres-solver/ceres-bin/lib -FVINS_ThirdPartyLib/ceres-solver/docs/source -FVINS_ThirdPartyLib/ceres-solver/examples/slam -FVINS_ThirdPartyLib/ceres-solver/examples/sampled_function -FVINS_ThirdPartyLib/ceres-solver/jni/config -FVINS_ThirdPartyLib/ceres-solver/data/libmv-ba-problems -FVINS_ThirdPartyLib/ceres-solver/data/nist -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen -FVINS_ThirdPartyLib/eigen3/Eigen/src -FVINS_ThirdPartyLib/ceres-solver/config/ceres/internal -FVINS_ThirdPartyLib/ceres-solver/include/ceres/internal -FVINS_ThirdPartyLib/ceres-solver/internal/ceres/generated -FVINS_ThirdPartyLib/ceres-solver/internal/ceres/gtest -FVINS_ThirdPartyLib/ceres-solver/internal/ceres/miniglog -FVINS_ThirdPartyLib/ceres-solver/internal/ceres/gmock -FVINS_ThirdPartyLib/ceres-solver/docs/source/_templates -FVINS_ThirdPartyLib/ceres-solver/examples/slam/pose_graph_3d -FVINS_ThirdPartyLib/ceres-solver/examples/slam/pose_graph_2d -FVINS_ThirdPartyLib/ceres-solver/examples/slam/common -FVINS_ThirdPartyLib/ceres-solver/jni/config/ceres -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/CXX11 -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src -FVINS_ThirdPartyLib/eigen3/Eigen/src/CholmodSupport -FVINS_ThirdPartyLib/eigen3/Eigen/src/misc -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core -FVINS_ThirdPartyLib/eigen3/Eigen/src/SparseLU -FVINS_ThirdPartyLib/eigen3/Eigen/src/OrderingMethods -FVINS_ThirdPartyLib/eigen3/Eigen/src/plugins -FVINS_ThirdPartyLib/eigen3/Eigen/src/Householder -FVINS_ThirdPartyLib/eigen3/Eigen/src/PardisoSupport -FVINS_ThirdPartyLib/eigen3/Eigen/src/SparseCore -FVINS_ThirdPartyLib/eigen3/Eigen/src/Jacobi -FVINS_ThirdPartyLib/eigen3/Eigen/src/SPQRSupport -FVINS_ThirdPartyLib/eigen3/Eigen/src/QR -FVINS_ThirdPartyLib/eigen3/Eigen/src/SparseQR -FVINS_ThirdPartyLib/eigen3/Eigen/src/SVD -FVINS_ThirdPartyLib/eigen3/Eigen/src/Cholesky -FVINS_ThirdPartyLib/eigen3/Eigen/src/UmfPackSupport -FVINS_ThirdPartyLib/eigen3/Eigen/src/IterativeLinearSolvers -FVINS_ThirdPartyLib/eigen3/Eigen/src/LU -FVINS_ThirdPartyLib/eigen3/Eigen/src/Geometry -FVINS_ThirdPartyLib/eigen3/Eigen/src/SuperLUSupport -FVINS_ThirdPartyLib/eigen3/Eigen/src/MetisSupport -FVINS_ThirdPartyLib/eigen3/Eigen/src/StlSupport -FVINS_ThirdPartyLib/eigen3/Eigen/src/SparseCholesky -FVINS_ThirdPartyLib/eigen3/Eigen/src/Eigenvalues -FVINS_ThirdPartyLib/eigen3/Eigen/src/PaStiXSupport -FVINS_ThirdPartyLib/ceres-solver/internal/ceres/miniglog/glog -FVINS_ThirdPartyLib/ceres-solver/jni/config/ceres/internal -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/CXX11/src -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/MatrixFunctions -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/LevenbergMarquardt -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/AutoDiff -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/NumericalDiff -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/NonLinearOptimization -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/Skyline -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/BVH -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/SpecialFunctions -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/Splines -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/KroneckerProduct -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/IterativeSolvers -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/FFT -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/EulerAngles -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/SparseExtra -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/Polynomials -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/MoreVectorization -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/Eigenvalues -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/products -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/util -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/functors -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch -FVINS_ThirdPartyLib/eigen3/Eigen/src/LU/arch -FVINS_ThirdPartyLib/eigen3/Eigen/src/Geometry/arch -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/CXX11/src/util -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/CXX11/src/ThreadPool -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/CXX11/src/TensorSymmetry -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/CXX11/src/Tensor -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/SpecialFunctions/arch -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/SSE -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/CUDA -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/ZVector -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/Default -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/AVX512 -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/AVX -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/NEON -FVINS_ThirdPartyLib/eigen3/Eigen/src/Core/arch/AltiVec -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/CXX11/src/TensorSymmetry/util -FVINS_ThirdPartyLib/eigen3/unsupported/Eigen/src/SpecialFunctions/arch/CUDA -F/Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/ThirdParty -filelist /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/iScout.LinkFileList -Xlinker -rpath -Xlinker @executable_path/Frameworks -dead_strip -Xlinker -object_path_lto -Xlinker /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/iScout_lto.o -Xlinker -export_dynamic -Xlinker -no_deduplicate -stdlib=libc++ -fobjc-arc -fobjc-link-runtime -L/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/swift/iphoneos -L/usr/lib/swift -Xlinker -add_ast_path -Xlinker /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/iScout.swiftmodule -framework Foundation /Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/Resources/boost.a -ljpeg -framework Accelerate -framework UIKit -framework QuartzCore -framework CoreImage -framework CoreMedia -framework CoreVideo -lceres -framework AssetsLibrary -framework AVFoundation -framework opencv2 -framework CoreMotion -framework GLKit -framework CoreGraphics -framework OpenGLES -Xlinker -dependency_info -Xlinker /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/iScout_dependency_info.dat -o /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Products/Debug-iphoneos/iScout.app/iScout



duplicate symbol '_OBJC_IVAR_$_AppDelegate._window' in:

  /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/AppDelegate-9BBA97070544062E.o

duplicate symbol '_OBJC_IVAR_$_AppDelegate._persistentContainer' in:

  /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/AppDelegate-9BBA97070544062E.o

duplicate symbol '_OBJC_CLASS_$_AppDelegate' in:

  /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/AppDelegate-9BBA97070544062E.o

duplicate symbol '_OBJC_METACLASS_$_AppDelegate' in:

  /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/AppDelegate-9BBA97070544062E.o

duplicate symbol '_main' in:

  /Users/kangyixiao/Library/Developer/Xcode/DerivedData/iScout-dduqjqfqbpboowalwfvpspkqphih/Build/Intermediates.noindex/iScout.build/Debug-iphoneos/iScout.build/Objects-normal/arm64/main-29D808328192F74B.o

ld: 5 duplicate symbols for architecture arm64

clang: error: linker command failed with exit code 1 (use -v to see in
```

vocation)

参考：https://www.cnblogs.com/xiaoyouPrince/p/5260378.html

![截屏2020-08-30 下午2.38.18](ISout调试笔记.assets/截屏2020-08-30 下午2.38.18.png)



典型：

**Showing All Errors Only**

```c#
 "ceres::Problem::AddResidualBlock(ceres::CostFunction*, ceres::LossFunction*, double*, double*, double*, double*, double*, double*)", referenced from:
```

可能的解决方案：

https://github.com/HKUST-Aerial-Robotics/VINS-Mobile/issues/54

https://github.com/HKUST-Aerial-Robotics/VINS-Mobile/issues/117

楼主遇到的问题为：

![截屏2020-08-30 下午2.37.55](ISout调试笔记.assets/截屏2020-08-30 下午2.37.55.png)

楼主解决方法

![截屏2020-08-30 下午2.33.41](ISout调试笔记.assets/截屏2020-08-30 下午2.58.17.png)



Bug5:Apple Mach-O Linker Error

一共23个

<img src="ISout调试笔记.assets/截屏2020-08-29 下午10.34.05.png" alt="截屏2020-08-29 下午10.34.05" style="zoom:33%;" />

错误原因：MAC下原工程更换编译环境后，若出现“**apple mach-o linker error "" referenced from.....**”错误，有可能是原工程没有加armv6，或者问题出现在Ohter Linker Flags 这个属性上。















### Bug5:simulator 编译错误

错误类型：

- 1./Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/iScout/CameraUtils.m:33:6: <u>Block will be retained by the captured object</u>
- /Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/iScout/feature_manager.cpp:9:10: <u>In file included from</u> /Users/kangyixiao/Desktop/PRP/iSout_develop/iScout的副本2_work_on/iScout/iScout/feature_manager.cpp:9:



参考：https://www.jianshu.com/p/ca1dc5ce92a2 发现类型2可能和block 有关

可能的解决方案，但是不知道怎么加：https://www.xuebuyuan.com/2061394.html










