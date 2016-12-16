# zhanqi-video-downloader
用于下载战旗tv录播视频的脚本，按分段下载，完成后自动合并。

## 使用方法-单视频
1. 确保有Python2.7运行环境。
2. 在脚本所在目录打开命令行，输入```python main.py danji/2015/11/50099```并运行。第三个参数是唯一视频id，可从视频url中获取。
3. 下载完成后在video文件夹找到下载的视频。

## 使用方法-多视频
1. 确保有Python2.7运行环境。
2. 编辑main.py，找到main函数中vid_list变量，将视频的唯一标识id填入列表中。可填入多个。
3. 运行main.py。
4. 下载完成后在video文件夹找到下载的视频。

## 特点
1. 预先检查当前视频总分段数。
2. 间隔1秒显示当前分段下载进度，同时显示当前分段数和总分段数。
3. 单个视频所有分段下载完成后，自动合成。
4. 纯控制台，没有GUI。在控制台观察进度。
5. 单线程。可以同时运行多个脚本实现多进程。
6. 暂不支持断点续传，但是可以手动更改start变量值来确定开始分段数。
7. 请求失败时自动重试。
8. 可以接受参数传入。
9. 只支持下载720P（超清）视频。
