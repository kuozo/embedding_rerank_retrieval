本项目是针对RAG中的Retrieve阶段的召回技术及算法效果所做评估实验。使用主体框架为`LlamaIndex`，版本为0.9.21.

Retrieve Method：

- BM25 Retriever
- Embedding Retriever
- Ensemble Retriever
- Ensemble Retriever + Cohere Rerank

## 数据

## 评估结果

BM25 Retriever Evaluation:

| retrievers      | hit_rate           | mrr                | cost_time          |
|-----------------|--------------------|--------------------|--------------------|
| bm25_top_1_eval | 0.7975077881619937 | 0.7975077881619937 | 461.2770080566406  |
| bm25_top_2_eval | 0.8535825545171339 | 0.8255451713395638 | 510.3020668029785  |
| bm25_top_3_eval | 0.9003115264797508 | 0.8411214953271028 | 570.6708431243896  |
| bm25_top_4_eval | 0.9158878504672897 | 0.8450155763239875 | 420.72606086730957 |
| bm25_top_5_eval | 0.940809968847352  | 0.8500000000000001 | 388.5960578918457  |

Embedding Retriever Evaluation:

| retrievers           | hit_rate           | mrr                | cost_time          |
|----------------------|--------------------|--------------------|--------------------|
| embedding_top_1_eval | 0.6074766355140186 | 0.6074766355140186 | 67.68369674682617  |
| embedding_top_2_eval | 0.6978193146417445 | 0.6526479750778816 | 60.84489822387695  |
| embedding_top_3_eval | 0.7320872274143302 | 0.6640706126687436 | 59.905052185058594 |
| embedding_top_4_eval | 0.778816199376947  | 0.6757528556593978 | 63.54880332946777  |
| embedding_top_5_eval | 0.794392523364486  | 0.6788681204569056 | 67.79217720031738  |

Ensemble Retriever Evaluation:

| retrievers          | hit_rate           | mrr                | cost_time          |
|---------------------|--------------------|--------------------|--------------------|
| ensemble_top_1_eval | 0.7009345794392523 | 0.7009345794392523 | 1072.7379322052002 |
| ensemble_top_2_eval | 0.8535825545171339 | 0.7741433021806854 | 1088.8781547546387 |
| ensemble_top_3_eval | 0.8940809968847352 | 0.7928348909657321 | 980.7949066162109  |
| ensemble_top_4_eval | 0.9190031152647975 | 0.8016614745586708 | 935.1701736450195  |
| ensemble_top_5_eval | 0.9376947040498442 | 0.8078920041536861 | 868.2990074157715  |

Ensemble Retriever + Rerank Evaluation:

| retrievers                 | hit_rate           | mrr                | cost_time         |
|----------------------------|--------------------|--------------------|-------------------|
| ensemble_rerank_top_1_eval | 0.8348909657320872 | 0.8348909657320872 | 2140632.404088974 |
| ensemble_rerank_top_2_eval | 0.9034267912772586 | 0.8785046728971962 | 2157657.287120819 |



## 改进方案

1. Query Transform
2. HyDE