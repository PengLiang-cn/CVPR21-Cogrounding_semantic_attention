# CVPR21-Cogrounding_semantic_attention

### Co-Grounding Networks with Semantic Attention for Referring ExpressionComprehension in Videos (CVPR 2021).

Project page: https://sijiesong.github.io/co-grounding/

Check out our [paper](<https://arxiv.org/abs/2103.12346>) here.


### Prerequisites
* Python 3
* Pytorch >= 0.4.1
* Others (OpenCV, scipy, etc.)

### Getting started
* Train CG-SL-Att. on VID 
```
python train_semantic_attention_cogrounding.py  --data_root  ./data  --dataset VID --gpu GPUID --savename SAVENAME_FOR_YOUR_MODEL  --batch_size BATCHSIZE --lstm
```

* Test CG-SL-Att. on VID (model acc: 59.48):

Please download trained models from [BaiduYun](<https://pan.baidu.com/s/1IMy9aISnsxw_wY8siEyEYg>)(Extraction code：p98p) or [GoogleDrive](<>)To be uploaded), then put the models under ./saved_models .

```
python train_semantic_attention_cogrounding.py  --data_root  ./data  --dataset VID --gpu GPUID --savename VID_cogrounding_semantic_attn  --batch_size BATCHSIZE --lstm --test --resume ./saved_models/VID_cogrounding_semantic_attn.pth.tar
```

* Train SL-Att. on RefCOCO
```
python train_semantic_attention_visual_grounding.py --data_root  ./data  --dataset unc --gpu GPUID --savename SAVENAME_FOR_YOUR_MODEL --batch_size BATCHSIZE --lstm
```

* Test SL-Att. on RefCOCO (model acc: val/testA/testB 77.65/80.75/73.37):

Please download trained models and the put the models under ./saved_models as above.
```
python train_semantic_attention_visual_grounding.py --data_root  ./data  --dataset unc --gpu GPUID --savename Refcoco_grounding_semantic_attn --batch_size BATCHSIZE --lstm --test --resume ./saved_models/RefCOCO_semantic_attn.pth.tar
```

### Todo
- [ ] Upload training models
- [ ] Upload data file
- [ ] Upload post-processing scripts


### Related projects

* [One-stage visual grounding](<https://github.com/zyang-ur/onestage_grounding>)


### Citation
If you use this code for your research, please cite our paper:

```
@inproceedings{cogrounding_2021_CVPR,
author = {Song, Sijie and Lin, Xudong and Liu, Jiaying and Guo, Zongming and Chang, Shih-Fu},
title = {Co-Grounding Networks with Semantic Attention for Referring Expression Comprehension in Videos},
booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
month = {June},
year = {2021}
}
```
