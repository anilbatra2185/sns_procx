<div align="center">

<h2><a href="https://arxiv.org/abs/2311.15964"><image src="./assets/eccv.png" alt="ECCV 2024" width=5%/> Efficient Pre-training for Localized Instruction Generation of Videos</a></h2>

[Anil Batra](https://anilbatra2185.github.io/), [Davide Moltisanti](https://www.davidemoltisanti.com/research/), [Laura Sevilla-Lara](https://laurasevilla.me/), [Marcus Rohrbach](https://rohrbach.vision/), [Frank Keller](https://homepages.inf.ed.ac.uk/keller/)

</div>

<h5 align="center">

[![arXiv](https://img.shields.io/badge/Arxiv-2311.15964-AD1C18.svg?logo=arXiv)](https://arxiv.org/abs/2311.15964)
[![Dataset](https://img.shields.io/badge/%F0%9F%A4%97%20Dataset-Sieve%20%26%20Swap-blue)](https://huggingface.co/datasets/anilbatra/sieve_and_swap)  <br>

</h5>

## Abstract
In this work we propose *Sieve & Swap* technique, to automatically generate high quality pre-training data for the recipe domain: (i) Sieve: filters irrelevant transcripts and (ii) Swap: acquires high quality text by replacing transcripts with human-written instruction from a text-only recipe dataset. The resulting dataset is three orders of magnitude smaller than current web-scale datasets but enables efficient training of large-scale models. Alongside *Sieve & Swap*, we propose Procedure Transformer (ProcX), a model for end-to-end step localization and instruction generation for procedural videos. When pre-trained on our curated dataset, this model achieves state-of-the-art performance on YouCook2 and Tasty while using a fraction of the training data.

<p align="center">
  <image src="./assets/sieve_n_swap.png" alt="sieve and swap approach" width=60%/>
</p>


## Dataset
***Pre-Training*** : [HowTo100M](https://www.di.ens.fr/willow/research/howto100m/), [RecipeNLG](https://github.com/Glorf/recipenlg)

***Downstream Task*** : [YouCook2](http://youcook2.eecs.umich.edu/), [Tasty](https://cvml.comp.nus.edu.sg/tasty/download.html)

***Download*** : Sieve and Swap dataset along with processed features can be downloaded from :hugs: [Hugging Face](https://huggingface.co/datasets/anilbatra/sieve_and_swap).

## Code

*Coming Soon!*

## :page_facing_up: Citation

If you find this project useful in your research, please consider cite:
```BibTeX

@misc{batra2024sns,
      title={Efficient Pre-training for Localized Instruction Generation of Videos}, 
      author={Anil Batra and Davide Moltisanti and Laura Sevilla-Lara and Marcus Rohrbach and Frank keller},
      year={2024},
      eprint={2311.15964},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

### Licenses
This code is released under the MIT License.
The licenses for datasets used in the paper are available at the following links: [HowTo100M](https://github.com/antoine77340/howto100m/blob/master/LICENSE), [YouCook2](https://github.com/LuoweiZhou/ProcNets-YouCook2/blob/master/LICENSE), and [Tasty](https://cvml.comp.nus.edu.sg/tasty/download.html).


### :dizzy: Acknowledgement

Thanks to the open source of the following projects:

[PDVC](https://github.com/OpenGVLab/InternVideo), [VidChapter](https://github.com/OpenGVLab/unmasked_teacher), [Lightning-Hydra-Template](https://github.com/ashleve/lightning-hydra-template).