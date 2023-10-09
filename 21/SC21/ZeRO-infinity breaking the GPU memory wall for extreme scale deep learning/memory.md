ZeRO: Memory Optimizations Toward Training Trillion Parameter Models. SC’20

ZeRO-Offload: Democratizing Billion-Scale Model Training. ATC'21

ZeRO-infinity: breaking the GPU memory wall for extreme scale deep learning. SC’21

LightSeq2: Accelerated Training for Transformer-Based Models on GPUs. SC'22

PatrickStar: Parallel Training of Pre-Trained Models via Chunk-Based Dynamic Memory Management. TPDS'23

Efficient Memory Management for Large Language Model Serving with PagedAttention



ZeRO:zero-dp(将模型状态平分，只更新自己负责的部分)+zero-r(MP删除冗余激活)

ZeRO-Offload:cpu(模型状态，参数更新，adam优化), gpu(参数，向前和向后计算), zero-2, MP只有对应参数在cpu上更新

ZeRO-infinity:gpu-cpu-NVMe，tile，聚合带宽，通信重叠

STRONGHOLD:动态加载模型状态，通信重叠，cpu多优化器更新参数，为第一个工作窗口的层保留GPU缓冲区，多核数据并行单参数

PatrickStar:块通信，动态内存分配，重用块