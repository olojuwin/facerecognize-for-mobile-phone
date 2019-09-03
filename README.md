# facerecognize-for-mobile-phone
适用于移动端的人脸识别模型，计算量于mobilefacenet相同，但megaface上提升了2%+。我训练的mobilefacenet在megaface VER上比原作者
高出了2%,因为训练的数据和方法不一样。

## 模型在各个数据集上表现如下：
|Methods|Flops (112x112)|LFW|CFP-FP|AgeDB|Megaface-Id|Megaface-Ver@1e-6|备   注
|:----|:----|:-----|:----|:----|:-----|:-----|:-----|
|MobileFaceNet440,R|440M|99.70+|96.70+|96.95+|92.85+|94.20+|未开源
|ZW350|356M|99.70+|96.82+|97.00+|93.90+|94.70+|未开源
|ZW400|404M|99.70+|96.95+|97.00+|94.46+|95.60+|未开源
|MobileFaceNet600,R|612M|99.76+|97.60+|97.50+|95.14+|95.98+|已开源
|ZW440|444M|99.76+|97.30+|97.40+|95.25+|96.00+|已开源

## Megafce测试结果图
zw440-id
![zw440-id](https://raw.githubusercontent.com/olojuwin/facerecognize-for-mobile-phone/master/img/zw443m-ID.jpg)

![zw440-ver](https://raw.githubusercontent.com/olojuwin/facerecognize-for-mobile-phone/master/img/zw443m-ver.jpg)

zw440-ver


## 速度比对测试
### 设备：i5-6500(暂时没有移动设备测试)
|Methods|Openvino|opencv单线程|
|:----|:----|:-----|
|MobileFaceNet600,R|6ms|141ms|
|ZW440|7ms|80ms

### 移动设备
经过测试，zw440并没有Mobilefacenet600M快.感谢[moli](https://github.com/moli232777144)的测试


## 模型地址
模型包含mxnet ncnn  caffe 三种格式
[Baidu Drive](https://pan.baidu.com/s/1E27uWe4deWsE0va1u1LhrQ)   提取码：b0dm 


## 训练数据
https://github.com/deepinsight/insightface/tree/master/iccv19-challenge

## 参考项目
https://github.com/deepinsight/insightface

https://github.com/happynear/FaceVerification

https://github.com/Tencent/ncnn

https://github.com/cypw/MXNet2Caffe

## Todo

没有做速度方面考虑，后期跟进改善。
