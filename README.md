# FishSynthesis
1st place project at UCSC Santa Cruz AI challenge sponsored by Egnyte. An image classification task trained on output from Stable Diffusion's text-to-image model, fine-tuned on dreambooth. Trained on 5% of original data (150/9000) and synthetically generated results with impressive performance.

## Output
Output from fine-tuned Stable Diffusion model using Google Dreambooth and [this kaggle dataset](https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset). Finetuned using approach from [TheLastBen](https://github.com/TheLastBen/fast-stable-diffusion). Model uploaded as [HuggingFace Pipeline](https://huggingface.co/arnavkartikeya/fakedmarinedata). 

![Real vs Fake Images](real-fake-compare.jpeg)

## Training Results
Results for training CNN on 150 real images -- Real-CNN
Results for training CNN on 150 real images plus synthetic data -- Synthetic-CNN
Results for Synthetic-CNN with better training practices (ReduceLROnPlateau, other Keras Callback features) -- Improved Synthetic CNN

