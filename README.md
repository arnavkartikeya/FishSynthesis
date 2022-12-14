# FishSynthesis
1st place project at UCSC Santa Cruz AI challenge sponsored by Egnyte. 

An image classification task trained on output from Stable Diffusion's text-to-image model, fine-tuned on dreambooth. Trained on 5% of original data (150/9000) and synthetically generated results with impressive performance (95% validation accuracy, results compared to pure real data in Training Results section).

## Output
Output from fine-tuned Stable Diffusion model using Google Dreambooth. Look at notes section for sources and resources for your own experimentation. 

![Real vs Fake Images](real-fake-compare.jpeg)

## Training Results
Results for training CNN on 150 real images -- Real-CNN

Results for training CNN on 150 real images plus synthetic data -- Synthetic-CNN

Results for Synthetic-CNN with better training practices (ReduceLROnPlateau, other Keras Callback features) -- Improved Synthetic CNN

![Results](results.png)

## Resources/Notes

Kaggle dataset compiled from 300 generate images across 9 species of fish can be found here [Kaggle Dataset](https://www.kaggle.com/datasets/arnavkartikeya/fakefishdata)

Data use for generation and test are from [This Kaggle Dataset](https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset).

Finetuned model uploaded as model uploaded as [HuggingFace Pipeline](https://huggingface.co/arnavkartikeya/fakedmarinedata). *Generating a single 512x512 image takes around 30 seconds on Colab Pro, the fakefishdata Kaggle Dataset was created on a Nautilus Cluster after 8 hours of training*.

Dreambooth finetuning implementation implemented from [TheLastBen on Github](https://github.com/TheLastBen/fast-stable-diffusion).

## Notebook instructions

Create a kaggle API token, instructions can be found [here](https://www.kaggle.com/docs/api). Upload the kaggle.json file to the same directory as the where the notebook is being run. Afterwards, all cells should be runnable. 
