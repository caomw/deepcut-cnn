# DeeperCut Part Detectors

This short documentation describes steps necessary to compile and run CNN-based body part detectors presented in the [DeeperCut paper](http://arxiv.org/abs/1605.03170):

**Eldar Insafutdinov, Leonid Pishchulin, Bjoern Andres, Mykhaylo Andriluka, and Bernt Schiele   
DeeperCut:  A Deeper, Stronger, and Faster Multi-Person Pose Estimation Model   
arXiv:1605.03170, 2016**	
For more information visit http://pose.mpi-inf.mpg.de

## Installation Instructions
- This code was developed under Linux (Debian wheezy, 64 bit) and was tested only in this environment.
- Build Caffe and Python bindings as described in the [official documentation](http://caffe.berkeleyvision.org/installation.html).
- Install Python Click package (required for demo only)		
```
pip install click
```
- Set PYTHONPATH variable	
```
cd <caffe_dir>
export PYTHONPATH=`pwd`/python
```

## Download Caffe Models
```
$ cd models/deepercut
$ ./download_models.sh
```

## Run Demo
```
$ cd python/pose
$ python ./pose_demo.py image.png --out_name=prediction
```

## Citing
```
@article{insafutdinov2016deepercut,
	author = {Eldar Insafutdinov and Leonid Pishchulin and Bjoern Andres and Mykhaylo Andriluka and Bernt Schieke},
	title = {DeeperCut: A Deeper, Stronger, and Faster Multi-Person Pose Estimation Model},
	journal = {arXiv},
	year = {2016},
	url = {http://arxiv.org/abs/1605.03170}
    }
@inproceedings{pishchulin16cvpr,
	author = {Leonid Pishchulin and Eldar Insafutdinov and Siyu Tang and Bjoern Andres and Mykhaylo Andriluka and Peter Gehler and Bernt Schiele},
	title = {DeepCut: Joint Subset Partition and Labeling for Multi Person Pose Estimation},
	booktitle = {IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
	year = {2016},
	url = {http://arxiv.org/abs/1511.06645}
}
```