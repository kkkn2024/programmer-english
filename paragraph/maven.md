## 1. maven settings.xml
### 1.1 `mirrors`元素注释
>    This is a list of mirrors to be used in downloading artifacts from remote repositories.

这是从远程仓库下载工件时使用的镜像列表。   
   
>    It works like this: a POM may declare a repository to use in resolving certain artifacts.      
However, this repository may have problems with heavy traffic at times, so people have mirrored it to several places.

它像这样工作：POM可以声明一个存储库，用于解析某些工件，
然而，此存储库有时可能会出现流量过大的问题，因此人们已将其镜像到多个位置。

>    That repository definition will have a unique id, so we can create a mirror reference for that repository, to be used as an alternate download site.   
The mirror site will be the preferred server for that repository.

该存储库定义将具有唯一ID，因此我们可以为该存储库创建镜像引用，以用作备用下载站点。
镜像站点将是该存储库的首选服务器。

### 1.2 `profiles`元素注释

<!-- profiles
>   | This is a list of profiles which can be activated in a variety of ways, and which can modify
   | the build process. Profiles provided in the settings.xml are intended to provide local machine-
   | specific paths and repository locations which allow the build to work in the local environment.
   |
   | For example, if you have an integration testing plugin - like cactus - that needs to know where
   | your Tomcat instance is installed, you can provide a variable here such that the variable is
   | dereferenced during the build process to configure the cactus plugin.
   |
   | As noted above, profiles can be activated in a variety of ways. One way - the activeProfiles
   | section of this document (settings.xml) - will be discussed later. Another way essentially
   | relies on the detection of a system property, either matching a particular value for the property,
   | or merely testing its existence. Profiles can also be activated by JDK version prefix, where a
   | value of '1.4' might activate a profile when the build is executed on a JDK version of '1.4.2_07'.
   | Finally, the list of active profiles can be specified directly from the command line.
   |
   | NOTE: For profiles defined in the settings.xml, you are restricted to specifying only artifact
   |       repositories, plugin repositories, and free-form properties to be used as configuration
   |       variables for plugins in the POM.
   |
   |-->