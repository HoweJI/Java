# Java
Learning progress

1.install Spring Tool in Eclipse

    help->Eclipse Marketplace-> Spring Tools(aka Spring IDE...)
    also if you do not want to install this extension, also you could create the SpringBoot project from the https://start.spring.io/

      
2.install mybatis generator in Eclipse

    the same as above action
    

3.create a new project, also add web,sqlserver driver, mybatis and devtool

    web - for we project
    sqlserver driver - run with sql server JDBC
    mybatis - doc management tool
    devtool - hot deploy

4.config mybatis

    pom.xml file :
    <plugin>
        <groupId>org.mybatis.generator</groupId>
        <artifactId>mybatis-generator-maven-plugin</artifactId>
        <configuration>
            <verbose>true</verbose>
            <overwrite>true</overwrite>
        </configuration>
    </plugin>

    create a new generatorConfig.xml file :
    <?xml version="1.0" encoding="UTF-8"?>

    <!DOCTYPE generatorConfiguration PUBLIC "-//mybatis.org//DTD MyBatis Generator Configuration 1.0//EN"

            "http://mybatis.org/dtd/mybatis-generator-config_1_0.dtd">
    <!-- 配置生成器 -->
    <generatorConfiguration>
        <!--classPathEntry:数据库的JDBC驱动,换成你自己的驱动位置 可选 -->
        <classPathEntry
            location="D:\Java\Maven_Repository\com\microsoft\sqlserver\mssql-jdbc\7.4.1.jre8\mssql-jdbc-7.4.1.jre8.jar" />
        <!-- 一个数据库一个context,defaultModelType="flat" 大数据字段，不分表 -->
        <context id="jiahao" targetRuntime="MyBatis3"
            defaultModelType="flat">
            <!-- jdbc连接 -->
            <jdbcConnection
                driverClass="com.microsoft.sqlserver.jdbc.SQLServerDriver"
                connectionURL="jdbc:sqlserver://localhost:1433;DatabaseName=Jiahao"
                userId="admin" password="admin" />
            <!-- 类型转换 -->
            <javaTypeResolver>
                <!-- 是否使用bigDecimal， false可自动转化以下类型（Long, Integer, Short, etc.） -->
                <property name="forceBigDecimals" value="false" />
            </javaTypeResolver>
            <!-- 生成实体类地址 -->
            <javaModelGenerator targetPackage="com.jiahao.vo"
                targetProject="D:\Eclipse\eclipse-workspace\springboot_mybatis_mvn_sqlserver\src\main\java">
                <!-- 是否让schema作为包的后缀 -->
                <property name="enableSubPackages" value="false" />
                <!-- 从数据库返回的值去掉前后空格 -->
                <property name="trimStrings" value="true" />
            </javaModelGenerator>
            <table tableName="USER" domainObjectName="UserVO">
                <property name="useActualColumnNames" value="true" />
            </table>
        </context>
    </generatorConfiguration>



    reference：https://blog.csdn.net/m0_37871296/article/details/89477921
    any tort, i will remove this link

5.when you want to use the org.json, please remind to follow the step from https://mvnrepository.com/artifact/org.json/json/20190722

    i have tested the other options several time, it doesn't work
    when i copy this dependency from website, it works!!!!!!