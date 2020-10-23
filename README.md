# Introduction
This is the official source code for **Dual Semantic Relations Attention Network(DSRAN)** proposed in our journal paper [Learning Dual Semantic Relations with Graph Attention for Image-Text Matching (TCSVT 2020)](https://arxiv.org/abs/2010.11550). It is built on top of the [VSE++](https://github.com/fartashf/vsepp) in PyTorch.

Codes will be available soon.

**The results on MSCOCO and Flicke30K dataset:(With BERT or GRU)**
<table>
  <tr>
    <td>GRU</td>
    <td colspan="3">Image-to-Text</td>
    <td colspan="3">Text-to-Image</td>
    <td></td>
  </tr>
  <tr>
    <td>Dataset</td>
    <td>R@1</td>
    <td>R@5</td>
    <td>R@10</td>
    <td>R@1</td>
    <td>R@5</td>
    <td>R@10</td>
    <td>Rsum</td>
  </tr>
  <tr>
    <td>MSCOCO-1K</td>                   
    <td>80.4</td>
    <td>96.7</td>
    <td>98.7</td>
    <td>64.2</td>
    <td>90.4</td>
    <td>95.8</td>
     <td>526.2</td>
  </tr>
  <tr>
    <td>MSCOCO-5K</td>      
    <td>57.6</td>
    <td>85.6</td>
    <td>91.9</td>
    <td>41.5</td>
    <td>71.9</td>
    <td>82.1</td>
     <td>430.6</td>
  </tr>
  <tr>  
    <td>Flickr30k</td>            
    <td>79.6</td>
    <td>95.6</td>
    <td>97.5</td>
    <td>58.6</td>
    <td>85.8</td>
    <td>91.3</td>
    <td>508.4</td>
  </tr>
</table>

<table>
  <tr>
    <td>BERT</td>
    <td colspan="3">Image-to-Text</td>
    <td colspan="3">Text-to-Image</td>
    <td></td>
  </tr>
  <tr>
    <td>Dataset</td>
    <td>R@1</td>
    <td>R@5</td>
    <td>R@10</td>
    <td>R@1</td>
    <td>R@5</td>
    <td>R@10</td>
    <td>Rsum</td>
  </tr>
  <tr>
    <td>MSCOCO-1K</td>       
    <td>80.6</td>
    <td>96.7</td>
    <td>98.7</td>
    <td>64.5</td>
    <td>90.8</td>
    <td>95.8</td>
     <td>527.1</td>
  </tr>
  <tr>
    <td>MSCOCO-5K</td>      
    <td>57.9</td>
    <td>85.3</td>
    <td>92.0</td>
    <td>41.7</td>
    <td>72.7</td>
    <td>82.8</td>
     <td>432.4</td>
  </tr>
  <tr>  
    <td>Flickr30k</td>      
    <td>80.5</td>
    <td>95.5</td>
    <td>97.9</td>
    <td>59.2</td>
    <td>86.0</td>
    <td>91.9</td>
    <td>511.0</td>
  </tr>
</table>

## Requirements and Installation
We recommended the following dependencies.
*  Python 3.6
*  PyTorch 1.1.0
*  NumPy (>1.12.1)
*  torchtext
*  pycocotools
*  nltk

## Download data

Download the raw images, pre-computed image features, pre-trained bert models and pre-trained DSRAN models. As for the raw images, they can be downloaded form [VSE++](https://github.com/fartashf/vsepp).

```
wget http://www.cs.toronto.edu/~faghri/vsepp/data.tar
wget http://www.cs.toronto.edu/~faghri/vsepp/vocab.tar
```
We refer to the path of extracted files for `data.tar` as `$DATA_PATH` while only raw images are use which are `coco` and `f30k`.

For pre-computed image features, they can be obtained from [VLP](https://github.com/LuoweiZhou/VLP).
### Data Structure
```
├── data/
|   ├── coco/           /* MSCOCO raw images
|   |   ├── images/
|   |   |   ├── train2014/
|   |   |   ├── val2014/
|   |   ├── annotations/
|   ├── f30k/           /* Flickr30K raw images
|   |   ├── images/
|   |   ├── dataset_flickr30k.json
|   ├── joint-pretrain/           /* pre-computed image features
|   |   ├── COCO/
|   |   |   ├── region_feat_gvd_wo_bgd/
|   |   |   |   ├── feat_cls_1000/
|   |   |   |   ├── coco_detection_vg_thresh0.2_feat_gvd_checkpoint_trainvaltest.h5
|   |   |   ├── annotations/
|   |   ├── flickr30k/
|   |   |   ├── region_feat_gvd_wo_bgd/
|   |   |   |   ├── trainval/
|   |   |   |   ├── flickr30k_detection_vg_thresh0.2_feat_gvd_checkpoint_trainvaltest.h5
|   |   |   ├── annotations/
```

## Train new models

## Evaluate trained models

## Acknowledgement

## Reference

If DSRAN is useful for your research, please cite our paper:

```
@ARTICLE{9222079,
  author={K. {Wen} and X. {Gu} and Q. {Cheng}},
  journal={IEEE Transactions on Circuits and Systems for Video Technology}, 
  title={Learning Dual Semantic Relations with Graph Attention for Image-Text Matching}, 
  year={2020},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/TCSVT.2020.3030656}}
```

## License

[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
