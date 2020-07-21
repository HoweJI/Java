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
    
4.config web env in eclipse
  i am using the 2020-06 eclipse, due to the clean initial env, i need to install most of the packages myse:lf.
  firstly, please update the mirror in the eclipse, in order to get the max internet speed.(i am using http://mirror.bit.edu.cn/eclipse/)
  
    help->install new software->work with ---- add a new for above mirror.
    select the "Web, XML, Java EE and OSGi Enterprise Development"
      -JST Server Adapters/JST Server Adapter Extensions/JST Server UI    server component
      -Eclipse Java EE Develpoper Tools/Eclipse Java Web Develpoper Tools/Eclipse Web Develpoper Tools/Eclipse XML Develpoper Tools/Eclipse XSL Develpoper Tools    java env
      (XSL is a XML data mapping software)
    right click->build path-> Libraries-> JRE   select the local JRE for developing
5.create maven project in the Eclipse
  we may could not find the Archetype first time.
  please use the mvn help:system to set up the initial environment for maven.
  
    windows->prefreences->Maven->Installation add a new to the maven package
    windows->prefreences->maven->user settings(use your personal setting.xaml)
  
  if it does not work also, select the internal type in archetype.it will download related package itself.
  
    The superclass "javax.servlet.http.HttpServlet" was not found on the Java Build Path
    -build path->add library->server runtime-> add your tomcat
    Description	Resource	Path	Location	Type Build path specifies execution environment J2SE-1.5.
    -modify the JRE in the build path
    Dynamic Web Module also need change
6.config tomcat in eclipse

    build path->libraries->add server run time->add you tomcat
    if the character displays error with chinese in cmd, please update the tomcat/conf/logging.properties file java.util.logging.ConsoleHandler.encoding = GBK(previous is UTF-8)
7.new a package in the src/main/java named as com.jiahao.servlet(we use this package to store all servlet file.)
8.define the initial page
    
      <welcome-file-list>
  	    <welcome-file>index.jsp</welcome-file>
      </welcome-file-list>
      due to the tomcat setting in conf/we.xml, we only could named the initial jsp as "index".
      <welcome-file-list>
        <welcome-file>index.html</welcome-file>
        <welcome-file>index.htm</welcome-file>
        <welcome-file>index.jsp</welcome-file>
      </welcome-file-list>
