# [Idea2Img](https://idea2img.github.io/) <img src="./icon.png" width="5%"/>
[Idea2Img: Iterative Self-Refinement with GPT-4V(ision) for Automatic Image Design and Generation](https://arxiv.org/pdf/2310.08541.pdf)

by [Zhengyuan Yang](http://zhengyuan.info/), [Jianfeng Wang](https://scholar.google.com/citations?user=vJWEw_8AAAAJ&hl=en), [Linjie Li](https://scholar.google.com/citations?user=WR875gYAAAAJ&hl=en), [Kevin Lin](https://sites.google.com/site/kevinlin311tw/me), [Chung-Ching Lin](https://www.microsoft.com/en-us/research/people/chunglin/), [Zicheng Liu](https://zicliu.wixsite.com/mysite), and [Lijuan Wang](https://www.microsoft.com/en-us/research/people/lijuanw/)


### Introduction
Built upon GPT-4V(ision), [Idea2Img](https://arxiv.org/pdf/2310.08541.pdf) is a multimodal iterative self-refinement system that enhances any T2I model for automatic image design and generation, enabling various new image creation functionalities togther with better visual qualities.

<p align="center">
  <img src="https://idea2img.github.io/images/teaser.png" width="75%"/>
</p>

### Citation

    @article{yang2023idea2img,
      title={Idea2img: Iterative self-refinement with gpt-4v (ision) for automatic image design and generation},
      author={Yang, Zhengyuan and Wang, Jianfeng and Li, Linjie and Lin, Kevin and Lin, Chung-Ching and Liu, Zicheng and Wang, Lijuan},
      journal={arXiv preprint arXiv:2310.08541},
      year={2023}
    }

### Prerequisites

* Obtain the public [OpenAI GPT-4V API key](https://platform.openai.com/docs/guides/vision) and setup T2I inference accordingly, e.g., [SDXL](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0).

## Installation

1. Clone the repository

    ```
    git clone https://github.com/zyang-ur/idea2img.git
    ```

### Running
2. Inference prompts will be read from ``--testfile``. ``<IMG>`` is a separator token inserted between image-image and image-text.

    ```
    mkdir output
    python idea2img_pipeline.py --api_key OAI_GPT4V_Key --testfile testsample.txt --fewshot --select_fewshot
    ```

### Results
3. Generated results and intermediate steps will be saved to ``output`` folder.

<p align="center">
  <img src="./main_de3.png" width="75%"/>
</p>