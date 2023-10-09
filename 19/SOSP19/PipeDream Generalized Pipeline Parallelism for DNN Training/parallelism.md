PipeDream: Fast and Efficient Pipeline Parallel DNN Training

GPipe: Easy Scaling with Micro-Batch Pipeline Parallelism

GPipe: efficient training of giant neural networks using pipeline parallelism. NIPS’19

PipeDream: generalized pipeline parallelism for DNN training SOSP’19

HetPipe: Enabling Large DNN Training on (Whimpy) Heterogeneous GPU Clusters through Integration of Pipelined Model Parallelism and Data Parallelism. ATC'20

Memory-Efficient Pipeline-Parallel DNN Training. ICML'21.

Megatron-LM: Training multi-billion parameter language models using model parallelism

Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM. SC’21

DAPPLE: A Pipelined Data Parallel Approach for Training Large Models. PPoPP'21

Chimera: efficiently training large-scale neural networks with bidirectional pipelines. SC'21

Out-Of-Order BackProp: An Effective Scheduling Technique for Deep Learning. EUROSYS'22

Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning. osdi’22

Unity: Accelerating DNN Training Through Joint Optimization of Algebraic Transformations and Parallelization. osdi’22

Tesseract: Parallelize the Tensor Parallelism Efficiently. ICPP’22

Galvatron: Efficient Transformer Training over Multiple GPUs Using Automatic Parallelism. VLDB’22

Elastic Averaging for Efficient Pipelined DNN Training. PPoPP’23

Merak: An Efficient Distributed DNN Training Framework With Automated 3D Parallelism for Giant Foundation Models. TPDS’23

https://github.com/ConnollyLeon/awesome-Auto-Parallelism



GPipe:microbatch

BSP:处理一次输入(microbatch?minibatch)同步(平均梯度)一次

PipeDream:1f1b，更新后的参数不能马上使用

HetPipe:1f1b+WSP

Using Megatron-LM:tp(切分乘法)+pp(同步pipedream+一个gpu对应多个stage)+dp

Chimera:两条流水线(一个顺序一个逆序)，扩展micro数量（平衡前后向时间），扩展流水线数量（stage-worker映射），dp
