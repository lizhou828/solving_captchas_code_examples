## 原文地址
    https://blog.csdn.net/shebao3333/article/details/78808066

## 准备工作

    1. 安装Python3，配好环境变量
    
    2. 安装OpenCV 3 w/ Python extensions
       推荐使用官方文档的安装方式： https://www.pyimagesearch.com/opencv-tutorials-resources-guides/
        
    3. 安装一些必须的第三方库
        pip install numpy
        pip install imutils
        pip install sklearn
        pip install tensorflow
        pip install keras
        pip install opencv-python==3.4.5  opencv-python(请用whl文件的方式安装，或者指定版本安装)
        
        在windows机上运行程序时，
        Tensorflow安装在导入模块时会出现ImportError: DLL load failed: 找不到指定的模块的问题：
        具体的解决方法是安装 Microsoft Visual C++ 2017 Redistributable
        附上百度云安装链接：https://pan.baidu.com/s/1FoFqH01_YkG54z6XFc9HRg
 

### Step 1: 从每张验证码图片中提取单个字符
    运行如下命令：
    python3 extract_single_letters_from_captchas.py
    提取的结果会放在"extracted_letter_images"文件夹里


### Step 2:训练神经网络识别单个字符
    运行如下命令：
    python3 train_model.py
    训练结果会写入 "captcha_model.hdf5" 、 "model_labels.dat"文件中


### Step 3: 使用模型来识别验证码
    运行如下命令：
    python3 solve_captchas_with_model.py
    


