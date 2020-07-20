# Training

For the training dataset folder, specify the folder to the base that contains a train and validation folder.

```shell
./distributed_train.sh 2 /imagenet -b 64 --model resnet50 --sched cosine --epochs 200 --lr 0.05 --remode pixel --reprob 0.6 --aug-splits 3 
```

# Inference

Specify the folder containing only validation images, not the base dir as in training script.

```shell
python inference.py /imagenet/validation/ --model mobilenetv3_100 --checkpoint ./output/model_best.pth.tar
```
