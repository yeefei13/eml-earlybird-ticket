Enter cifar/weight-level to run basic resnet model on cifar.

Use -a to sepcific which model being used(preresnet), --depth to spcific depth of the model(layers). Can leave other default with 91% accuracy. 

Example of argument:

python cifar.py -d cifar10 --epochs 200 --train-batch 128 --drop 0.5 --schedule 40 80 120 160 180 -a preresnet --depth 20



network slimming

baseline 
python main.py --arch resnet --depth 20 --dataset cifar10

prune
python resprune.py --dataset cifar10 --no-cuda --depth 20 --percent 0.3 --model C:\Users\yifei\OneDrive\桌面\rethinking-network-pruning-master\cifar\network-slimming\eb_result\epoch_10.pth.tar --save ./SPrune_10ep_0.3

finetune
python main_finetune.py --refine C:\Users\yifei\OneDrive\桌面\rethinking-network-pruning-master\cifar\network-slimming\SPrune_10ep_0.3\pruned.pth.tar --dataset cifar10 --arch resnet --depth 20 --save ./eb_finetune_10ep_0.3       