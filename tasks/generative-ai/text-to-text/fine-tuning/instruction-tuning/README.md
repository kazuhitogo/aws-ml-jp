# SageMaker での LLM Instruction Tuning

このプロジェクトには、SageMaker 上で Large Language Models (LLM) をプロンプトでファインチューニング/デプロイするためのサンプルノートブックが含まれています。

3種類のノートブックがあります。

- `*_Inference.ipynb`: 事前学習済みモデルをデプロイする。
- `*_Finetune.ipynb`: 通常のファインチューニングを行い、モデルをデプロイする。
- `*_LoRA.ipynb`: LoRA メソッドを用いたファインチューニングを行い、モデルをデプロイする。

モデルは利用しやすいように以下のような形式の json で学習できるように標準化されています。

```
[
    {
        "input": "",
        "instruction": "",
        "output": ""
    },
    ...
]
```

## ノートブック一覧

| ノートブック | 説明 |
| -------- | ----------- |
| [Alpaca_LoRA.ipynb](Transformers/Alpaca_LoRA.ipynb) | Alpaca-LoRA を Alpaca Dataset で LoRA チューニングとデプロイ |
| [Alpaca_Inference.ipynb](Transformers/Alpaca_Inference.ipynb) | Alpaca-LoRA をデプロイ |
| [Alpaca_LoRA_ja.ipynb](Transformers/Alpaca_LoRA_ja.ipynb) | Alpaca-LoRA を日本語 Alpaca Dataset で LoRA チューニングとデプロイ |
| [Alpaca_Inference_ja.ipynb](Transformers/Alpaca_Inference_ja.ipynb) | 日本語 Alpaca-LoRA をデプロイ |
| [Cerebras_Finetune.ipynb](Transformers/Cerebras_Finetune.ipynb) | Cerebras を Dolly Dataset でファインチューニングとデプロイ |
| [Cerebras_Inference.ipynb](Transformers/Cerebras_Inference.ipynb) | Cerebras をデプロイ |
| [Cerebras_LoRA.ipynb](Transformers/Cerebras_LoRA.ipynb) | Cerebras を Dolly Dataset で LoRA チューニングとデプロイ |
| [Cerebras_LoRA_ja.ipynb](Transformers/Cerebras_LoRA_ja.ipynb) | Cerebras を 日本語 Dolly Dataset で LoRA チューニングとデプロイ |
| [StableLM_Inference.ipynb](Transformers/StableLM_Inference.ipynb) | StableLM をデプロイ |
| [StableLM_LoRA.ipynb](Transformers/StableLM_LoRA.ipynb) | StableLM を Dolly Dataset で LoRA チューニングとデプロイ |
| [Dolly_v2_Inference.ipynb](Transformers/Dolly_v2_Inference.ipynb) | Dolly v2 をデプロイ |
| [Dolly_v2_LoRA.ipynb](Transformers/Dolly_v2_LoRA.ipynb) | Dolly v2 を Dolly Dataset で LoRA チューニングとデプロイ |
| [OpenCALM_Inference_ja.ipynb](Transformers/OpenCALM_Inference_ja.ipynb) | OpenCALM をデプロイ |
| [OpenCALM_Inference_jaqket.ipynb](Transformers/OpenCALM_Inference_jaqket.ipynb) | OpenCALM をデプロイし [JAQKET](https://www.nlp.ecei.tohoku.ac.jp/projects/jaqket/) データセットに対し推論 |
| [OpenCALM_LoRA_ja.ipynb](Transformers/OpenCALM_LoRA_ja.ipynb) | OpenCALM を Dolly Dataset で LoRA チューニングとデプロイ |
| [OpenCALM_LoRA_jaqket.ipynb](Transformers/OpenCALM_LoRA_jaqket.ipynb) | OpenCALM を [JAQKET](https://www.nlp.ecei.tohoku.ac.jp/projects/jaqket/) で LoRA チューニングとデプロイ |
| [Rinna_Neox_Inference_ja.ipynb](Transformers/Rinna_Neox_Inference_ja.ipynb) | Rinna NeoX をデプロイ |
| [Rinna_Neox_LoRA_ja.ipynb](Transformers/Rinna_Neox_LoRA_ja.ipynb) | Rinna NeoX を Dolly Dataset で LoRA チューニングとデプロイ |
| [RWKV_Inference.ipynb](Transformers/RWKV_Inference.ipynb) | RWKV のデプロイ |
| [MPT_Inference.ipynb](Transformers/MPT_Inference.ipynb) | MPT のデプロイ |
| [MPT_LoRA.ipynb](Transformers/MPT_LoRA.ipynb) | MPT を Dolly Dataset で LoRA チューニングとデプロイ |
| [MPT_LoRA_ja.ipynb](Transformers/MPT_LoRA_ja.ipynb) | MPT を 日本語 Dolly データセットで LoRA チューニングとデプロイ |
| [RWKV_Finetune.ipynb](RWKV/RWKV_Finetune.ipynb) | RWKV を Dolly Dataset でファインチューニングとデプロイ |
| [RWKV_LoRA.ipynb](RWKV/RWKV_Finetune.ipynb) | RWKV を Dolly Dataset で LoRA チューニングとデプロイ |
| [RWKV_LoRA_ja.ipynb](RWKV/RWKV_Finetune.ipynb) | RWKV を 日本語 Dolly データセットで LoRA チューニングとデプロイ |
| [RWKV_Inference.ipynb](RWKV/RWKV_Inference.ipynb) | RWKV のデプロイ |
| [RWKV_Inference_ja.ipynb](RWKV/RWKV_Inference_ja.ipynb) | 日本語 RWKV Raven のデプロイ |

比較評価用

| ノートブック | 説明 |
| -------- | ----------- |
| [OpenAI_Inference_Chat_Completions_jaqket.ipynb](OpenAI/OpenAI_Inference_Chat_Completions_jaqket.ipynb) | OpenAI ChatCompletions API で [JAQKET](https://www.nlp.ecei.tohoku.ac.jp/projects/jaqket/) データセットに対し推論 |
| [OpenAI_Inference_jaqket.ipynb](OpenAI/OpenAI_Inference_Completions_jaqket.ipynb) | OpenAI Completions API で [JAQKET](https://www.nlp.ecei.tohoku.ac.jp/projects/jaqket/) データセットに対し推論 |
| [OpenAI_Finetune_jaqket.ipynb](OpenAI/OpenAI_Finetune_jaqket.ipynb) | OpenAI API を [JAQKET](https://www.nlp.ecei.tohoku.ac.jp/projects/jaqket/) でファインチューニングし推論 |
| [OpenAI_Price_Calculator.ipynb](OpenAI/OpenAI_Price_Calculator.ipynb) | OpenAI API の価格を、データのトークン数から試算するための Notebook |
