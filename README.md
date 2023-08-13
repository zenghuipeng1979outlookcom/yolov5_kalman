# 实验原理：
### 1 使用IOU算法和卡尔曼滤波实现对yolov5s的目标框进行跟踪
###2 模拟检测失败丢框的情况，测试下来可以用卡尔曼滤波算法在跟踪的基础上进行补框。

# 使用方法：
解压zip，运行  python3 detect.py --source ~/Videos/testvideo1.mp4 --view-img 

# 参考库：
### 1 上游库基于yolov5s tag v6.0
### 2 参考：https://github.com/liuchangji/kalman-filter-in-single-object-tracking 

# 配置修改：
### 1 Q，R，iou阈值值，根据实际情况测试，丢框率和目标移动轨迹随机性不同，值的配置也不同
### 2 模拟丢框比例修改randata变量的条件（模拟丢框率，默认是50%）
### 3 修改sleep时间，如果推理太快看不清过程可以增加，或单步调试

# FAQ：
### 报错怎么办：
请参考yolov5s安装依赖，python我使用3.6,cuda12.1,yolov5s代码使用V6.0tag

# Demo：
<iframe 
src="./result.mp4" 
scrolling="no" 
border="0" 
frameborder="no" 
framespacing="0" 
allowfullscreen="true" 
height=600 
width=800> 
</iframe>