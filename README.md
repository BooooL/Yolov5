# Yolov5
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE) <br>

YoloV5 implemented by TensorFlow2 , with support for training, evaluation and inference. <br>

> **NOT perfect** project currently, but I will continue to improve this, so you might want to watch/star this repo to revisit. Any contribution is highly welcomed<br>

![demo](./data/sample/demo1.png)

<!-- | Model | Test Size | AP<sup>val</sup> | AP<sub>50</sub><sup>val</sup> | AP<sub>75</sub><sup>val</sup> | AP<sub>S</sub><sup>val</sup> | AP<sub>M</sub><sup>val</sup> | AP<sub>L</sub><sup>val</sup> | yaml | weights |
| :-- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -->

## Key Features
- minimal Yolov5 by pure tensorflow2
- yaml file to configure the model
- custom data training
- mosaic data augmentation
- label encoding by iou or wh ratio of anchor
- positive sample augment
- multi-gpu training
- detailed code comments
- full of drawbacks with huge space to improve

## Usage
### Clone and install requirements
```
$ git clone git@github.com:LongxingTan/Yolov5.git
$ cd Yolov5/
$ pip install -r requirements.txt
```
<!-- ### Download pretrained weights
```
$ cd weights/
$ bash download_weights.sh
``` -->
### Download VOC
```
$ data/scripts/get_voc.sh
$ cd yolo
$ python dataset/prepare_data.py
```

<!-- ### Download COCO
```
$ cd data/
$ bash get_coco_dataset.sh
``` -->
### Train
```
$ python train.py
```
If you want to train on custom dataset, PLEASE note the input data should like this:
```
image_dir/001.jpg x_min, y_min, x_max, y_max, class_id x_min2, y_min2, x_max2, y_max2, class_id2
```
And maybe new anchor need to be created depending on the data, don't forget to change the nc(number classes) in yolo-yaml.

### Inference
```
$ python detect.py
```

## References and Further Reading
- [yolov5](https://github.com/ultralytics/yolov5)
- [PyTorch_YOLOv4](https://github.com/WongKinYiu/PyTorch_YOLOv4)
- [yolov3-tf2](https://github.com/zzh8829/yolov3-tf2)
- [tensorflow-yolov3](https://github.com/YunYang1994/tensorflow-yolov3)
