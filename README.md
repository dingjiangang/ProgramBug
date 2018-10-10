1.https://blog.csdn.net/kaixinjiuxing666/article/details/80321124  ubuntu创建虚拟环境    
2.https://blog.csdn.net/qq_40994114/article/details/79464549 安装cudnn7.1  
3.conda env create --file environment_cpu.yml  
4.https://blog.csdn.net/xiaoming0018/article/details/80346895   破解pycharm  
5.cuda动态库链接  
sudo cp /usr/local/cuda-8.0/lib64/libcudnn.so.6.0.20 /usr/local/lib/libcudnn.so.6.0.20 && sudo ldconfig  
sudo cp /usr/local/cuda-8.0/lib64/libcudart.so.8.0 /usr/local/lib/libcudart.so.8.0 && sudo ldconfig  
sudo cp /usr/local/cuda-8.0/lib64/libcublas.so.8.0 /usr/local/lib/libcublas.so.8.0 && sudo ldconfig  
sudo cp /usr/local/cuda-8.0/lib64/libcurand.so.8.0 /usr/local/lib/libcurand.so.8.0 && sudo ldconfig  
6.sudo pip install -r /home/dingjiangang/caffe/python/requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple  
pip 按照requirements安装依赖，且添加清华大学镜像源  
7. sudo ln -s /usr/bin/python3.5 /usr/bin/python  删除2.7python 如何让3.5生效  
8.export LD_LIBRARY_PATH="$HOME/caffe/build/lib:$LD_LIBRARY_PATH"  添加caffe的python环境变量   
9.cmake .. -DCMAKE_INSTALL_PREFIX=/home/dingjiangang/projects/nihao/third_pa
rty/yaml-cpp-yaml-cpp-0.5.3/gen   


 
 


