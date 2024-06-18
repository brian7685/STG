
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
<<< HowToCaption[‘---39MFGZ-k’]   

{
'start': [12, 19, 29, 25, 55, 81, 82], 
'end': [20, 27, 37, 33, 63, 89, 90], 
'text': [
[‘Show how to unload a 12-gauge shotgun’], 
[‘Loading a 12-gauge shotgun’], 
[‘Demonstrating how to unload a 12-gauge shotgun', 'A better way to unload a gun’], 
[‘Putting another round into the gun', 'The danger of loading a gun the usual way’], 
[‘Loading the gun safely', 'Short stroke to load the gun', 'Loading the gun today’], 
[‘Lifting up the bar to extract rounds’], 
[‘Going forward and lifting up the bar to extract rounds'] 
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


