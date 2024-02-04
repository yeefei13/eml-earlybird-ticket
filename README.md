Enter cifar/weight-level to run basic resnet model on cifar.

Use -a to sepcific which model being used(preresnet), --depth to spcific depth of the model(layers). Can leave other default with 91% accuracy. 

Example of argument:

python cifar.py -d cifar10 --epochs 200 --train-batch 128 --drop 0.5 --schedule 40 80 120 160 180 -a preresnet --depth 20
