# SIGIR2020_PeterRec
# Parameter-Efficient Transfer from Sequential Behaviors for User Profiling and Recommendation
```
@article{yuan2020parameter,
  title={Parameter-Efficient Transfer from Sequential Behaviors for User Modeling and Recommendation},
  author={Yuan, Fajie and He, Xiangnan and Karatzoglou, Alexandros and Zhang, Liguang},
  journal={arXiv preprint arXiv:2001.04253},
  year={2020}
}
```

PeterRec_cau_parallel.py: PeterRec with causal cnn and parallel insertion

PeterRec_cau_serial.py: PeterRec with causal cnn and serial insertion

PeterRec_noncau_parallel.py: PeterRec with noncausal cnn and parallel insertion

PeterRec_noncau_serial.py: PeterRec with causal cnn and serial insertion



NextitNet_TF_Pretrain.py: Petrained by NextItNet [0] (i.e., causal cnn)

GRec_TF_Pretrain.py: Petrained by the encoder of GRec [1] (i.e., noncausal cnn)


## Demo Steps:

First:  python NextitNet_TF_Pretrain.py

After convergence(you can stop it once the pretrained model are saved!)

Second: python PeterRec_cau_serial.py

Make sure PeterRec is converged, sometimes it will keep relatively stable for several iteractions and then keep increasing again.

or

First:  python GRec_TF_Pretrain.py

After convergence

Second: python PeterRec_noncau_parallel.py

## Running our paper:
Replacing the demo dataset with our public datasets (including both pretraining and finettuning):

You will reproduce the results reported in our paper using our papar settings, including learning rate, embedding size,
dilations, batch size, etc. Note that the results reported in the paper are based on the same hyper-parameter settings for fair comparison and ablation tests. You may further finetune hyper-parameters to obtatin the best performance. For example, we use 0.001 as learning rate, but you may find 0.0001 performs better, although all insights in the paper keep consistent.




Related work:
```
[1]
@inproceedings{yuan2019simple,
  title={A simple convolutional generative network for next item recommendation},
  author={Yuan, Fajie and Karatzoglou, Alexandros and Arapakis, Ioannis and Jose, Joemon M and He, Xiangnan},
  booktitle={Proceedings of the Twelfth ACM International Conference on Web Search and Data Mining},
  pages={582--590},
  year={2019}
}
```
```
[2]
@inproceedings{yuan2020future,
  title={Future Data Helps Training: Modeling Future Contexts for Session-based Recommendation},
  author={Yuan, Fajie and He, Xiangnan and Jiang, Haochuan and Guo, Guibing and Xiong, Jian and Xu, Zhezhao and Xiong, Yilin},
  booktitle={Proceedings of The Web Conference 2020},
  pages={303--313},
  year={2020}
}
```
