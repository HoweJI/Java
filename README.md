# Java
Learning progress

1.install JAVA jre in PC
  install from Oracle
  config the JAVA_HOME, CLASSPATH, Path in the environment variables.

    a.JAVA_HOME
      D:\Java\Java      //depends on your install config

    b.CLASSPATH
      .;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;         //please pay attention to the "." in the front

    c.Path
      %JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;
      
after all config, input "java -version" on commond prompt

2.install Eclipse
3.install Maven

    Download Link :http://maven.apache.org/download.cgi
    
  it's more convient to down load the Binary Zip.
  after installation, we may need create the local repository.once you build mvn project, IDE will firstly search the jar package from local repository, if not exists, will download from remote repository.
  besides, "mvn install" will package the project and install to the local repository.
  
    modify as below in the setting.xaml file in conf.
    <localRepository>D:\Java\Maven_Repository</localRepository>
    
  
4.create maven project in the Eclipse
  we may could not find the Archetype first time.
  please use the mvn help:system to set up the initial environment for maven.
  
    windows->prefreences->Maven->Installation add a new to the maven package
    windows->prefreences->maven->user settings(use your personal setting.xaml)
  
  if it does not work also, select the internal type in archetype.it will download related package itself.
