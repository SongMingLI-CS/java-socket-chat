# Java 多线程聊天室

这是一个完全使用 Java SE 核心技术构建的多客户端、多线程聊天服务器和客户端应用程序。

## 🌟 主要功能 

* **多客户端连接:** 服务器使用多线程，可以同时处理多个客户端的连接和消息。
* **用户认证:** 基于 MySQL 数据库和 JDBC 的用户注册与登录功能。
* **图形用户界面:** 客户端使用 Java Swing 构建，提供了用户友好的聊天窗口。
* **实时消息:** 客户端之间可以实时发送和接收消息。
* **服务器日志:** 服务器会将关键事件（如用户登录、断开连接）记录到本地日志文件。
   
## 🛠️ 所用技术栈 (Technologies Used)

* **核心 (Core):** Java SE (JDK 11+)
* **网络 (Networking):** `java.net.Socket` 和 `java.net.ServerSocket` (TCP/IP 套接字编程)
* **并发 (Concurrency):** `java.lang.Thread` 和 `java.lang.Runnable` (Ch 24: 多线程)
* **数据库 (Database):** MySQL 8.0, JDBC
* **图形界面 (GUI):** Java Swing
* **输入输出 (IO):** `InputStream` / `OutputStream`, `BufferedReader` / `PrintWriter` (Ch 21-23: IO 体系)
    
* **高级:**
    * `java.lang.reflect.Proxy` (Ch 26: 动态代理 - 用于日志记录)
        (java.lang.reflect.Proxy (Ch 26: Dynamic Proxy - used for logging))
    * `java.lang.annotation.Annotation` (Ch 26: 注解)
        (java.lang.annotation.Annotation (Ch 26: Annotations))
    * `java.lang.reflect` (Ch 25: 反射)
        (java.lang.reflect (Ch 25: Reflection))
    * `java.util.function` (Ch 27: Lambda 表达式)
        (java.util.function (Ch 27: Lambda Expressions))
* **测试:** JUnit (Ch 25)

## 🚀 如何运行

### 1. 准备环境

1.  确保已安装 Java (JDK 11 或更高版本)。
    
2.  确保已安装并运行 MySQL 数据库。
   
3.  在 MySQL 中创建数据库: `CREATE DATABASE chat_system;`
    
4.  执行以下 SQL 语句创建 `users` 表:
    (Execute the following SQL to create the `users` table:)
    ```sql
    CREATE TABLE chat_system.users (
        id INT PRIMARY KEY AUTO_INCREMENT,
        username VARCHAR(50) NOT NULL UNIQUE,
        password VARCHAR(50) NOT NULL
    );
    ```

### 2. 运行服务器 

1.  克隆或下载本项目。
    
2.  在 IDE 中打开项目。
    
3.  (可选)修改 `DBUtil.java` 中的数据库连接信息（用户名、密码）。
   
4.  运行 `ServerMain.java` (或导出的 `Server.jar`)。
   
5.  您应该会在控制台看到 "服务器已启动..."。
 

### 3. 运行客户端

1.  运行 `ClientMain.java` (或导出的 `Client.jar`)。
  
2.  **您可以运行任意多个客户端实例。**
   
3.  在客户端窗口中注册一个新账户，然后登录。
    
4.  打开另一个客户端，用另一个账户登录，开始聊天。
  
