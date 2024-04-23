## cmake 构建

####  cmake有什么用？

cmake是用于实现多文件项目的编译和连接



#### 如何使用？

1. 在项目目录中创建CMakeLists.txt文件

2. 在文件中写入cmake版本，项目名称，需要连接的文件及目标文件

   ```cmake
   cmake_minimum_required(VERSION 3.28.0)
   
   project(test_project)
   
   add_executable(main main.cpp account.cpp account.h)  # 第一个为目标文件
   ```

3. 输入命令行

   ```cmd
   cmake .\ -G "MinGW Makefiles"  # .\为具体txt文件所在目录
   ```

   此时项目中会多出若干个文件和文件夹

   ![image-20240411102831705](C:\Users\xyx\AppData\Roaming\Typora\typora-user-images\image-20240411102831705.png)

4. 输入命令行

   ```cmd
   make
   ```

   生成执行文件

5. 运行可执行文件

   ```cmd
   .\main.exe
   ```

6. 完成项目的构建



#### cmake使用过程中出现的报错？

- ###### 执行cmake报错

  ![image-20240411103317420](C:\Users\xyx\AppData\Roaming\Typora\typora-user-images\image-20240411103317420.png)

  此时需要指明生成器，在后面添加  -G "MinGW Makefiles" 即可

  

  如果此时还报错，则需要将mingw64的bin目录配置到系统环境变量中

  ![image-20240411103611722](C:\Users\xyx\AppData\Roaming\Typora\typora-user-images\image-20240411103611722.png)

- 无法识别make命令

  ![image-20240411103822124](C:\Users\xyx\AppData\Roaming\Typora\typora-user-images\image-20240411103822124.png)

  mingw的bin目录下的mingw32-make.exe复制一份副本，再将副本名称改为make.exe即可



























