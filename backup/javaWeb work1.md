实训一：JavaWeb应用开发环境搭建与入门
一、实训目标
1. 理解JavaWeb开发的基本概念（JSP、Servlet、Tomcat）。
2. 掌握JDK与Tomcat服务器的安装、配置及环境变量设置。
3. 学会在IDEA中配置Tomcat并创建第一个Web项目。
4. 能够编写简单的HTML和JSP页面，并通过浏览器访问。

二、实训环境
- JDK 25（或相应版本）
- Apache Tomcat 11.0.18
- IntelliJ IDEA（社区版或旗舰版

三、实训内容与步骤
1. JDK安装与环境变量配置
- 安装JDK（路径须为全英文，如 `C:\Program Files\Java\jdk-25`）
- 配置系统环境变量：
  - `JAVA_HOME` = `C:\Program Files\Java\jdk-25`
  - `Path,` = `%JAVA_HOME%\bin`
2. Tomcat服务器安装与启动
- 解压或安装Tomcat，记录安装路径
- 启动服务器：进入 `bin` 目录，双击 `startup.bat`
- 访问测试：浏览器打开 `http://localhost:8080`
- **可选**：修改端口号（编辑 `conf/server.xml`，将8080改为80或其他）
- **解决控制台乱码**：修改 `conf/logging.properties` 中 `java.util.logging.ConsoleHandler.encoding` 为 `GBK`

3. 在IDEA中配置Tomcat
- 破解软件：将win2021-2025文件夹放置于C盘根目录
- 运行C:\win2021-2025\scripts中的uninstall-all-users.vbs卸载配置
- 运行C:\win2021-2025\scripts中的install-current-user.vbs安装纯净配置
- 打开并复制C:\win2021-2025\Activation_Code中的IntelliJ IDEA.txt中的激活码，粘贴至IDEA-帮助导航栏-管理订阅-激活码中进行破译
- 配置运行环境：
  - 运行 → 调试配置 → 添加“Tomcat Server（本地）”
  - 选择Tomcat安装目录，设置HTTP端口（如8080）
  - 部署：添加“工作”（exploded）类型的工件
- 保存配置并启动服务器
4. 创建第一个Web项目
- 在Tomcat的 `webapps` 目录下新建项目文件夹，如 `my_web`
- 项目结构：
  ```
  my_web/
  ├── WEB-INF/
  └── index.html   (或 index.jsp)
  ```
- 编写一个简单的HTML页面（或JSP页面），通过 `http://localhost:8080/my_web/` 访问

5. 编写JSP页面示例
```jsp
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head><title>第一个JSP</title></head>
<body>
  <h1>Hello JavaWeb!</h1>
  <% out.println("当前时间：" + new java.util.Date()); %>
</body>
</html>
```
四、常见问题提示
- **端口被占用**：修改 `server.xml` 中的端口号
- **控制台乱码**：按上述方法修改 `logging.properties` 为 GBK
- **IDEA无法识别Tomcat**：检查jdk版本是否正确，Tomcat安装版本是否正确
- **页面访问404**：确认项目放在 `webapps` 下，且URL路径正确
