# 拯救者无线网链接问题 
``` 
rfkill list all  
sudo modprobe -r ideapad_laptop 
```
在文件/etc/rc.local文件中添加命令
```
echo "123" |sudo modprobe -r ideapad_laptop
```

# cuda动态库链接 
```  
sudo cp /usr/local/cuda-8.0/lib64/libcudnn.so.6.0.20 /usr/local/lib/libcudnn.so.6.0.20 && sudo ldconfig  
sudo cp /usr/local/cuda-8.0/lib64/libcudart.so.8.0 /usr/local/lib/libcudart.so.8.0 && sudo ldconfig  
sudo cp /usr/local/cuda-8.0/lib64/libcublas.so.8.0 /usr/local/lib/libcublas.so.8.0 && sudo ldconfig  
sudo cp /usr/local/cuda-8.0/lib64/libcurand.so.8.0 /usr/local/lib/libcurand.so.8.0 && sudo ldconfig  
```  
# pip如何使用清华源安装第三方库
sudo pip install -r /home/dingjiangang/caffe/python/requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple    

# 如何引用不同版本的opencv  
将库安装在指定目录，在cmakelist里面添加  
```  
set(OpenCV_DIR /home/djg/opencv-3.2.0/share/OpenCV)   
find_package(OpenCV REQUIRED)   
include_directories(${OpenCV_INCLUDE_DIRS})   
target_link_libraries(nihao  ${OpenCV_LIBS} ) 
```   

# vscode  
## 一、vscode安装  
+ 通过官方PPA安装Ubuntu make  
```
sudo add-apt-repository ppa:ubuntu-desktop/ubuntu-make  
sudo apt-get update  
sudo apt-get install ubuntu-make  
```
- 使用命令安装visual studio code 
```  
umake ide visual-studio-code  
``` 
- 卸载已经安装的VSCode  
```
umake ide visual-studio-code  --remove 
``` 
- 启动vscode
``` 
sh /home/dingjiangang/.local/share/umake/ide/visual-studio-code/bin/code  
``` 
# ros安装教程  
- 添加源  
  + 打开一个控制台(Ctrl + Alt + T), 输入如下指令：
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'  
```
  + 设置秘钥:   
```
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116  
```
- 安装 ROS 
  + 首先确保系统软件处于最新版 
```
sudo apt-get update
```
  + 安装至尊豪华全功能版 
```
sudo apt-get install ros-kinetic-desktop-full
```
- 初始化ROS 
  + 初始化 rosdep 
```
sudo rosdep init
rosdep update
```
  + 初始化环境变量  
```
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```


