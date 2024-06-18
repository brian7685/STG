
# Grounding YouTube Dataset #
What, when, and where? -- Self-Supervised Spatio-Temporal Grounding in Untrimmed Multi-Action Videos from Narrated Instructions
[arxiv](https://arxiv.org/abs/2303.16990)


## Download:  

### Video dataset:  
 GroundingYouTube dataset that we use in the paper can be found [here](https://docs.google.com/uc?export=download&id=1wmJvkvqZoqsD8rvFVZ3KLV2vV9WXv89R) ~7.1GB
 
### Extracted frames:  
 The pre-extraced frames from the videos correspond to the annotation can be found [here](https://drive.google.com/file/d/1THpcXddk4SmNfTqeMujV7MxGIWeydO4H/view?usp=sharing)) ~2GB   

### Annotation:  
 The spatio-temporal annotation is in the *annotation* folder

 
## How To Use  

#### How to use filtered HowToCaption or HowToCaption-grounded datasets:  
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

### How to use unfiltered HowToCaption or HowToCaption-grounded datasets:  

The difference to standard HowToCaption dataset is that ‘text’ is list of lists of tuples of (string, score).

**Example**:
```
<<< HowToCaption[‘---39MFGZ-k’]

{
'start': [12, 19, 25, 29, 55, 54, 65, 81, 82, 105, 103], 
'end': [20, 27, 33, 37, 63, 62, 73, 89, 90, 113, 111], 
'text': [
[('Show how to unload a 12-gauge shotgun', 0.5699871778488159)], 
[('Loading a 12-gauge shotgun', 0.5876383185386658)], 
[('Unloading and removing a round from the chamber', 0.31276029348373413), ('Putting another round into the gun', 0.4805337190628052), ('The danger of loading a gun the usual way', 0.4611629843711853)],
[('Demonstrating how to unload a 12-gauge shotgun', 0.617999255657196), ('A better way to unload a gun', 0.5126216411590576)], 
[('Loading the gun safely', 0.539146363735199), ('Short stroke to load the gun', 0.5076732635498047), ('Loading the gun today', 0.4759426712989807)], 
[('Being nervous on camera', 0.3465729355812073), ('Nervousness on camera', 0.27738460898399353)], 
[('Extracting rounds by lifting up the bar', 0.41076189279556274)], 
[('Lifting up the bar to extract rounds', 0.4220432639122009)], 
[('Going forward and lifting up the bar to extract rounds', 0.42620745301246643)], 
[('A person is speaking and pointing out that there are no ramps present', 0.30187565088272095)], 
[('The speaker mentions that they can be found online', 0.30197498202323914), ('The speaker concludes the video by saying "WWE" and ending the video', 0.36031144857406616)]]
}
```


### Acknowledgement
* [BLIP](https://github.com/salesforce/BLIP) is the model for text-video encoder and score function
* [Vicuna](https://github.com/lm-sys/FastChat/tree/main) is open source instructional LLM to generate HowToCaption dataset
* [MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4) is open-source LLM with image conditioning  to generate HowToCaption-grounded dataset


If you're using HowToCaption or HowToCaption-grounded dataset in your research or applications, please cite using this BibTeX:

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


