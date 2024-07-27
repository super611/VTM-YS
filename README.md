# VTM-YS

Code for "Lightweight Multiobject Ship Tracking Algorithm Based on Trajectory Association and Improved YOLOv7tiny"



![gif](E:\DevProjects\PycharmProject\Dengzh\VTM-YS\gif.gif)




## Documentation

See below for quickstart examples.

<details open>
<summary>Install</summary>


Clone repo and install [requirements.txt](https://github.com/ultralytics/yolov5/blob/master/requirements.txt) in a [**Python>=3.7.0**](https://www.python.org/) environment, including [**PyTorch>=1.7**](https://pytorch.org/get-started/locally/).

```bash
git clone https://github.com/super611/VTM-YS  # clone
cd VTM-YS
pip install -r requirements.txt  # install
```


</details>

<details open>
<summary>Inference with track.py</summary>


Use pretrained yolov7tiny-vessel.pt to track MVI_1484_VIS.avi:

```bash
python track.py --yolo-weights yolov7/weights/yolov7tiny-vessel.pt --strong-sort-weights strong_sort/weights/osnet_x1_0_vessel.pth --source Video_Sample/MVI_1484_VIS.avi
```



</details>

<details open>
<summary>Training</summary>


The.yaml file for VTM-YS is located in the VTM-YS_YAML folder.

```bash
cd VTM-YS
cd yolov7
python train.py --cfg cfg/improve/yolov7-tiny-pplcnet-pconv-slimbipanet-ca.yaml --epochs 150 --weights 'yolov7-tiny.pt' --batch-size 32
```



![test_batch1_pred](E:\DevProjects\PycharmProject\Dengzh\VTM-YS\test_batch1_pred.jpg)


</details>




>>>>>>> 2154ae5 (first commit)
