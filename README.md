# BAFIS: A Human Preference Benchmark to assess Bias in Multilingual Text-to-Image Generation

BAFIS is a research project that aims to investigate how language differences influence bias in modern Text-to-Image models such as Stable Diffusion 3 Medium, FLUX.1-dev, Playground v2.5, Midjourney and DALL-E 3 and whether people can subjectively assess this bias.

As part of the project, we generated a dataset of synthetic images using the preceding models with multi-lingual text prompts from the MAGBIG dataset, which focuses on prompts for occupational portraits. The dataset is limited to images generated for the prompt languages English and German.

Additionally we added group prompts (e.g. "A photo of the faces of a group of accountants.") to these prompts resulting in a combined number of 1057 unique prompts.

For each prompt, we generated 4 images using the models mentioned above resulting in a total of 21140 high-quality PNG images at 1024×1024 resolution. These images serve as the basis for the evaluation by the participants of our user study.

The images are provided in the form of a filtered dataset. The dataset has been filtered using DeepFace (with YOLOv8 as the detection backend) to exclude images that lack discernible faces.

thumbnails.zip contains a small version of the dataset with PNG image thumbnails at 128x128 resolution.

bafis_images.zip contains the full version of the dataset with high-quality PNG images at 1024x1024 resolution.

Each version of the dataset includes a metadata.json file specifying image information regarding occupation, model, prompt_group (see MAGBIG), language and prompt.
