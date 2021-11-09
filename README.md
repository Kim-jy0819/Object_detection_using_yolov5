# Object_detection_using_yolov5
스마트 그리드를 위한 오브젝트 분류를 위하여 yolo v5를 활용해 커스텀 트레이닝을 실시하였습니다.

# 데이터 수집
roboflow.ai에서 이미지 데이터 라벨링 및 증식을 진행하였습니다.


# train
```
python train.py --img 416 --batch 16 --epochs 50 --data /content/data.yaml --cfg ./models/yolov5n.yaml --weights yolov5n.pt --name yolov5n_results
```

# inference
```
python detect.py --weights /content/yolov5/runs/train/yolov5n_results/weights/best.pt --source 0
```

