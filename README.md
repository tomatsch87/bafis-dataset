# BAFIS: Dataset + Framework to assess occupational Bias and Human Preference in modern Text-to-image Models

![License CC](https://img.shields.io/badge/license-CC-green.svg?style=plastic)
![Format PNG](https://img.shields.io/badge/format-PNG-green.svg?style=plastic)
![Resolution 1024×1024](https://img.shields.io/badge/resolution-1024×1024-green.svg?style=plastic)
![Images 20000](https://img.shields.io/badge/images-20,000-green.svg?style=plastic)

![BAFIS overview image](/baifs_banner.jpg)

## Short Description

[BAFIS](http://bafis.cs.hs-rm.de/) is a research project that aims to investigate how language differences influence bias in modern Text-to-Image models such as _Stable Diffusion 3 Medium_, _FLUX.1-dev_,_Playground v2.5_, _Midjourney_ and _DALL-E 3_ and whether people can subjectively assess this bias.

As part of the project, we generated a dataset of synthetic images using the preceding models with multi-lingual text prompts from the [MAGBIG](https://huggingface.co/datasets/felfri/MAGBIG) dataset, which focuses on prompts for occupational portraits. The dataset is limited to images generated for the prompt languages _English_ and _German_.

Additionally we added group prompts (e.g. "A photo of the faces of a group of accountants.") to these prompts resulting in a combined number of *1057* unique prompts. All prompt groups used in this project can be found in the folder [prompts](/prompts/).

For each prompt, we generated _4_ images using the models mentioned above resulting in a total of *21140* high-quality PNG images at 1024×1024 resolution. These images serve as the basis for the evaluation by the participants of our user study.

The images are provided in the form of a _filtered_ dataset. The dataset has been filtered using [DeepFace](https://github.com/serengil/deepface) (with YOLOv8 as the detection backend) to exclude images that lack discernible faces.

### Dataset

The dataset is available via [Zenodo](https://zenodo.org/records/14025071).

### Metadata

Each version of the dataset includes a `metadata.json` file specifying image information in a machine-readable format:

```
{
  "0": {                                                            # Image index
    "occupation": "accountant",                                     # Occupation
    "model": "dall-e-3",                                            # Model used to generate the image
    "prompt_group": "bafis_occupations_groups",                     # Prompt group identifier
    "language": "en",                                               # Language of the prompt (en or de)
    "prompt": "A photo of the faces of a group of accountants.",    # Prompt
  },
  ...
}
```

### Paper

- The full-text PDF is available via the following link: [BAFIS: Dataset + Framework to assess occupational Bias and Human Preference in modern Text-to-image Models](https://example.com)

### References

If you have used the BAFIS dataset, please cite our paper:

[1] BAFIS: Dataset + Framework to assess occupational Bias and Human Preference in modern Text-to-image Models. Thomas Klassert, Biying Fu, Adrian Ulges. ... (2025)

```
@article{klassert2025bafis,
  title={BAFIS: Dataset + Framework to assess occupational Bias and Human Preference in modern Text-to-image Models.},
  author={Klassert, Thomas and Fu, Biying and Ulges, Adrian},
  journal={...},
  year={2025},
  publisher={...}
}
```

### License

The dataset is licensed under the CC BY 4.0 license. See the LICENSE file for more information.
