# Autoresearch Lab — Day 1, 3.14

## Summary
今天成功搭建并稳定运行 autoresearch 实验环境，开始进行真实的模型结构搜索实验。通过连续实验发现：在固定训练时间预算下，降低模型深度可以显著提升 step efficiency，并成功把 val_bpb 从约 2.38 降到 2.18，建立了新的 winner baseline。

## Next Step
明天优先继续测试更小的模型结构（如进一步降低 depth 或 embedding 规模），目标是寻找新的 winner baseline，并尝试把 val_bpb 推进到 2.10 以下。