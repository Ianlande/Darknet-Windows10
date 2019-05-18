# Darknet-Windows10
Darknet for Windows10, cuda9.1,vs2017,opencv3.4.0 which had been compiled

------

## 使用方法
在`darknet-master\build\darknet\x64`下创建一个`.cmd`文件，填入如下格式的命令
### 训练
格式：
```
darknet.exe detector train (.data文件路径) (.cfg文件路径) -i 0 darknet53.conv.74
```
`-i 0`表示使用第一个`GPU`
例如:
```
darknet.exe detector train D:\\MyNetWork\\Vrep_yolov3_training\\cfg\\yolov3-vrep-ddpg-obj.data   D:\\MyNetWork\\Vrep_yolov3_training\\cfg\\yolov3-vrep-ddpg.cfg   -i 0   darknet53.conv.74

pause
```

------

### 测试
格式：
```
darknet.exe detector test (.data文件路径) (.cfg文件路径) -i 0 (backup文件中的权重文件路径)
```
例如:
```
darknet.exe detector test D:\\MyNetWork\\Vrep_yolov3_training\\cfg\\yolov3-vrep-ddpg-obj.data   D:\\MyNetWork\\Vrep_yolov3_training\\cfg\\yolov3-vrep-ddpg.cfg   -i 0  D:\\MyNetWork\\Vrep_yolov3_training\\backup\\yolov3-vrep-ddpg_2000.weights

pause
```
