# Java
Learning progress

1.install java package in vscode

    Java Extension Pack

      
2.install java package in vscode

    the same as above action
    JDK is better

3.create the springboot project from springboot initializer

    after creation, click the debug to run
    you may face the failure "Failed to configure a DataSource: 'url' attribute is not specified and no embedded datasource could be configured."
    just need to replace the comment above main function
    @SpringBootApplication(exclude = DataSourceAutoConfiguration.class)

4.after that, run this project, open the explore to http://localhost:8080/
  
    first step is done.
