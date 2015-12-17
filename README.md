# jenkins Docker container 

jdk version:java-8u66-jdk

### java
    插件：
       git(这里使用git作为版本控制)：scm-api.hpi、git-client.hpi、git.hpi
       工具：publish-over-ftp.hpi 和 publish-over-ssh.hpi


### android
    
    插件：
      必须安装的有： 
        git(这里使用git作为版本控制)：scm-api.hpi、git-client.hpi、git.hpi 
        android：port-allocator.hpi、android-emulator.hpi、analysis-core.hpi、android-lint.hpi 
        gradle(项目是使用Android Studio开发的)：gradle.hpi
      可选安装的有： 
        单元测试：junit.hpi 
        代码覆盖率：jacoco.hpi 
        代码查虫：findbugs.hpi 
        邮箱扩展：email-ext.hpi
    
    参考：http://blog.csdn.net/it_talk/article/details/50215089
 
