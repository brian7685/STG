
# Grounding YouTube Dataset #
What, when, and where? -- Self-Supervised Spatio-Temporal Grounding in Untrimmed Multi-Action Videos from Narrated Instructions
[arxiv](https://arxiv.org/abs/2303.16990)


## Download:  

### Video dataset:  
 GroundingYouTube dataset that we use in the paper can be found [here](https://docs.google.com/uc?export=download&id=1wmJvkvqZoqsD8rvFVZ3KLV2vV9WXv89R) ~7.1GB
 
### Extracted frames:  
 The pre-extraced frames from the videos correspond to the annotation can be found [here](https://drive.google.com/file/d/1THpcXddk4SmNfTqeMujV7MxGIWeydO4H/view?usp=sharing) ~2GB   

### Annotation:  
 The spatio-temporal annotation is in [box](annotations/box_anno.json) 
  
 
## How To Use  

#### How to use GroundingYouTube datasets:  
* Each file is a dictionary with video-ids as keys 
* For each video we provide ‘start’, ‘end’, and ‘text’ lists of the same lengths  
* ’start’ and ‘end’ correspond to starts and ends seconds of the clips in the video

  
To note: 
- ‘text’ is list of lists of strings as to the same position in the video can correspond several captions
- Starting seconds in ‘start’ list are not ordered; however, ‘end’ seconds always correspond  to ’start’ positions ordering


**Example**:   

```
<<< GroundingYouTube["-1okAudsnAc"]   

    {
        "76":
        {
            "box":
            [
                186,
                244,
                388,
                452
            ],
            "step": "crack eggs"
        },
        "77":
        {
            "box":
            [
                193,
                246,
                395,
                451
            ],
            "step": "crack eggs"
        },
        "86":
        {
            "box":
            [
                224,
                7,
                432,
                218
            ],
            "step": "pour egg whites"
        },
        "87":
        {
            "box":
            [
                246,
                131,
                450,
                335
            ],
            "step": "pour egg whites"
        },
        "88":
        {
            "box":
            [
                245,
                79,
                454,
                292
            ],
            "step": "pour egg whites"
        },
}
```


### Acknowledgement
* [MiningYouTube](https://github.com/hildekuehne/Mining_YouTube_dataset/tree/master) is the video dataset with temporal annotation.


If you're using GroundingYouTube in your research or applications, please cite using this BibTeX:

```
@InProceedings{Chen_2024_CVPR,
    author    = {Chen, Brian and Shvetsova, Nina and Rouditchenko, Andrew and Kondermann, Daniel and Thomas, Samuel and Chang, Shih-Fu and Feris, Rogerio and Glass, James and Kuehne, Hilde},
    title     = {What When and Where? Self-Supervised Spatio-Temporal Grounding in Untrimmed Multi-Action Videos from Narrated Instructions},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2024},
    pages     = {18419-18429}
}
```


### Licence: 
 
This repository is under Apache License. 


