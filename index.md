# Introduction

Digital image forensic has gained a lot of attention as it is becoming easier for anyone to make forged images. Several areas are concerned by image manipulation: a doctored image can increase the credibility of fake news, impostors can use morphed images to pretend being someone else. 

It became of critical importance to be able to recognize the manipulations suffered by the images. To do this, the first need is to be able to rely on reliable and controlled data sets representing the most characteristic cases encountered. The purpose of this work is to lay the foundations of a body of tests allowing both the qualification of automatic methods of authentication and detection of manipulations and the training of these methods.

Various techniques are involved in image manipulations, from simple global characteristics improvements (color enhancement, saturation, color remapping, contrast increase) to complex local forgeries (object incrustation or deletion, camouflage in-painting, morphing of structure) 

We propose here a novel Dataset (DEFACTO) containing four forgeries categories :
1. Copy and Move
2. Splicing
3. Object Removal
4. Morphing

This Dataset has been constructed over [MSCOCO](http://cocodataset.org/#home), and forgeries have been generated automatically.

# Copy-Move

![Example of Copy-Move](/img/cpmf_ex.png)

About 19000 copy-move forgeries are available under the copymove directory. Each copy-move is accompanied by two binary
masks.
One under the probe_mask subdirectory indicates the location of the forgery and one under the donor_mask indicates the 
location of the source within the image.


# Splicing

![Examples of Splicing](/img/sp_ex.png)

About 105000 splicing forgeries are available under the splicing directory. Each splicing is accompanied by two binary
masks.
One under the probe_mask subdirectory indicates the location of the forgery and one under the donor_mask indicates the 
location of the source. The external image can be found in the JSON file under the graph subdirectory.

# Object-Removal

![Examples of Object-Removal](/img/inpainting_ex_1.png)
About 25000 object-removal forgeries are available under the inpainting directory. Each object-removal is accompanied by two 
binary masks.
One under the probe_mask subdirectory indicates the location of the forgery and one under the inpaint_mask which is the mask
use for the inpainting algorithm.

# Morphing

![Examples of Face Morphing](/img/morph_ex.png)
About 40000 face morphing forgeries are available under the face morphing directory. Each face morphing is accompanied by 
two binary masks.
One under the probe_mask subdirectory indicates the location of the forgery and one under the donor_mask indicates the 
location of the source. The external image can be found in the JSON file under the graph subdirectory.

# Dataset access request

To get access to this Dataset, please fill in this [form](https://docs.google.com/forms/d/1G-xxLvBkykTnbkP1rKkWDazNrhrggosaHMhouncN4mk/). You will shortly receive a mail of confirmation and we will process your request.



# Reference

Please refer to the original paper :

>@INPROCEEDINGS{DEFACTODataset,
>AUTHOR="Gaël Mahfoudi and Badr Tajini and Florent Retraint and Fr{\'e}d{\'e}ric
>Morain-Nicolier and Jean Luc Dugelay and Marc Pic",
>TITLE="{DEFACTO:} Image and Face Manipulation Dataset",
>BOOKTITLE="27th European Signal Processing Conference (EUSIPCO 2019)",
>ADDRESS="A Coruña, Spain",
>DAYS=1,
>MONTH=sep,
>YEAR=2019
>}

And the [MSCOCO dataset](http://cocodataset.org/#home)
# License

The DEFACTO Consortium does not own the copyright of those images.
Please refer to the MSCOCO [terms of use](http://cocodataset.org/#termsofuse) for all images based on their Dataset.
This Dataset also contains images of persons gathered on [IMDB](https://www.imdb.com/). If any of this images
belongs to you and you wish it to be removed contact us at defacto.dataset@gmail.com.

