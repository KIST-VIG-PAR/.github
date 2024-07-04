<div align="center">
<h1>VIG Pedestrian Attribute Recognition <br> 인수인계 자료</h1>
</div>



<p align="center"> <video src="https://github.com/KIST-VIG-PAR/.github/assets/71140885/f919997c-615a-4781-9994-f94cfb5df5a4" width="100%"></p>

## Setup
모든 코드는 python 3.8.10, torch 2.1.0+cu121 에서 동작합니다.  
아래 [Code](#Code)에 각 코드에 필요한 셋업 가이드라인 및 모델 가중치가 있습니다.  
파일을 Github에 올릴 수 없는 경우 K-Drive에 업로드 해두었습니다.

## Dataset
이 레포지토리에 있는 실험을 하기 위해선 **PA100k, PETA, RAP2, Market1501, UPAR, 그리고 KIST 실외 데이터셋**이 필요합니다.  
데이터셋들은 [여기 (비밀번호: vigvig)](https://filesharelink.kist.re.kr/link/G8YC7jkS)에서 다운로드 받으실 수 있습니다.  
다운로드 받으실 수 없는 경우 **NAS (orange) server**에서 `aiid/dataset/re-id/Dataset/00_Attribute` 에서 찾아 다운로드 받으시면 됩니다.  
각 데이터셋의 폴더 구조는 아래와 같아야 합니다.  
```
home/data
├── PA100k                    
│   ├── data
│   ├── annotation.mat
│   ├── dataset_all.pkl
│   └── dataset_zs_run0.pkl   
├── PETA                    
│   ├── images
│   ├── dataset_all.pkl
│   └── dataset_zs_run0.pkl
├── RAP2                    
│   ├── RAP_annotation
│   ├── RAP_dataset
│   ├── dataset_all.pkl
│   └── dataset_zs_run0.pkl
├── Market1501                    
│   ├── bounding_box_test
│   ├── bounding_box_train
│   ├── gt_bbox
│   ├── gt_query
│   ├── query
│   └── ...
├── UPAR                    
│   └── dataset_all.pkl
├── kist_outdoor_trajectory                    
│   ├── cctv_2                       # cctv number
│   │   ├── 9_10                     # time
│   │   │   ├── trajectory number
│   │   │   │   ├── clips            # video folder
│   │   │   │   ├── 123123123.jpg
│   │   │   │   ├── 123123124.jpg
│   │   │   │   ├── 123123125.jpg
│   │   │   │   ├── ...
│   │   ├── 12_13
│   │   ├── 17_18
│   ├── cctv_3
│   └── ...
└── ...

```

## Code
### Ours
* [SEEM-PAR](https://github.com/KIST-VIG-PAR/SEEM-PAR.git)
### Baseline
* [SOLIDER](https://github.com/KIST-VIG-PAR/SOLIDER.git)
* [PromptPAR](https://github.com/KIST-VIG-PAR/PromptPAR.git)
### Others
* [Rethinking](https://github.com/valencebond/Rethinking_of_PAR/tree/master)
* [Label2Label](https://github.com/Li-Wanhua/Label2Label)
* [VTB](https://github.com/cxh0519/VTB)
  


## Results
### Inference Time
| MOdel | Inference Time <br> per 64 samples|
| --- | --- |
|SOLIDER|  0.19541s |
|PromptPAR | 0.32794s |
|SEEMPAR| 0.43812s |

### Visualization

시각화 자료는 SOLIDER, PromptPAR, SEEM-PAR 모델을 기반으로 합니다.   
다운로드 받을 수 없는 경우, 업로드 된 가중치를 통해 visualization 코드를 실행하면 같은 결과가 나옵니다.  

* [KIST 실외 데이터 패치별 시각화](https://filesharelink.kist.re.kr/link/c7NXubET) 비밀번호: vigvig
* [KIST 실외데이터 동영상 시각화](https://filesharelink.kist.re.kr/link/eOG0imRv) 비밀번호: vigvig


