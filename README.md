**Status:** Archive (code is provided as-is, no updates expected)

# gpt-2

Code from the paper ["Language Models are Unsupervised Multitask Learners"](https://d4mucfpksywv.cloudfront.net/better-language-models/language-models.pdf).

We have currently released small (124M parameter), medium (355M parameter), and large (774M parameter) versions of GPT-2<sup>*</sup>, with only the full model as of yet unreleased.  We have also [released a dataset](https://github.com/openai/gpt-2-output-dataset) for researchers to study their behaviors.

You can read about GPT-2 and release decisions in our [original blog post](https://blog.openai.com/better-language-models/) and [6 month follow-up post](https://openai.com/blog/gpt-2-6-month-follow-up/).

<sup>*</sup> *Note that our original parameter counts were wrong due to an error (in our previous blog posts and paper).  Thus you may have seen small referred to as 117M and medium referred to as 345M.*

## Usage

This repository is meant to be a starting point for researchers and engineers to experiment with GPT-2.

For basic information, see our [model card](./model_card.md).

### Some caveats

- GPT-2 models' robustness and worst case behaviors are not well-understood.  As with any machine-learned model, carefully evaluate GPT-2 for your use case, especially if used without fine-tuning or in safety-critical applications where reliability is important.
- The dataset our GPT-2 models were trained on contains many texts with [biases](https://twitter.com/TomerUllman/status/1101485289720242177) and factual inaccuracies, and thus GPT-2 models are likely to be biased and inaccurate as well.
- To avoid having samples mistaken as human-written, we recommend clearly labeling samples as synthetic before wide dissemination.  Our models are often incoherent or inaccurate in subtle ways, which takes more than a quick read for a human to notice.

### Work with us

Please [let us know](mailto:languagequestions@openai.com) if you’re doing interesting research with or working on applications of GPT-2!  We’re especially interested in hearing from and potentially working with those who are studying
- Potential malicious use cases and defenses against them (e.g. the detectability of synthetic text)
- The extent of problematic content (e.g. bias) being baked into the models and effective mitigations

## Development

HNG 6.0 ML Task

## Requirements

    fire>=0.1.3 - Fire 
    regex==2017.4.5 - For OpenAI GPT
    requests==2.21.0    - Used for downloading models over HTTP 
    tqdm==4.31.1    - progress bars in model download and training scripts
    torch>=0.4.1    - PyTorch
    boto3   - Accessing files from S3 directly.




## License

[MIT](./LICENSE)
