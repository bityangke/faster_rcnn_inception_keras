
also see "Common sw win10 openai pybullet tensorflow keras matlab deep l learning", 12/29/2019 note

the python script test_inception_keras.py works on tensorflow gpu 1.14 +
keras 2.3.1, or tensorflow cpu + keras 2.3.1

tf 1.12 or lower not work
source ~/bin/usepython3.sh 
/media/student/tf-gpu-src mounted
python3 test_inception_keras.py 

-------12/31/2019 work with rtx 2080 ----------
the test_inception_keras.py not work with rtx 2080 machine,
a libcudnn error, fixed by 
	config.gpu_options.allow_growth = True

this is tested on native and docker images. 
	native env: homepc, rtx 2080, 1tb ssd #5, sda19, nvidia 430.64 open src, cuda 10, cudnn 7, 
	docker images: same hardware, tensorflow/tensorflow:latest-gpu-py3, jwang3vsu/tensorflow:tf1.14-keras
