# l4tdockerbuild-f
building nvcr.io_nvidi_l4t_ml_r32.6.1-p3 to run triton server on jetson 
build the docker file using 
sudo docker build ./ -t < Docker name>:<Tag>
use the following command to run docker 
sudo docker run --gpus all -it --shm-size=2g --rm -v /home/:/home p3:v0.2
once build use the following command to copy the python folder from backends inside docker to the triton server backend folder 
cp /backends/python -r /tritonserver2.16.0-jetpack4.6/backends/
use the following command to run triton server 
/home/nano/Downloads/tritonserver2.16.0-jetpack4.6/bin/tritonserver --backend-directory=s/tritonserver2.16.0-jetpack4.6/backends/ --model-repository=
<path>
>>  
for instaling albumination without instlling scikit and open cv headless use the command 
  pip3 install --no-deps scikit-image albumentations
  
