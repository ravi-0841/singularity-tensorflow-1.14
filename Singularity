Bootstrap: docker
From: tensorflow/tensorflow:1.14.0-gpu-py3

%environment
  # use bash as default shell
  SHELL=/bin/bash
  export SHELL

%setup
  # runs on host - the path to the image is $SINGULARITY_ROOTFS

%post
  # post-setup script

  # load environment variables
  . /environment

  # use bash as default shell
  echo 'SHELL=/bin/bash' >> /environment

  # make environment file executable
  chmod +x /environment

  # default mount paths
  mkdir /scratch /data 


  # additional packages
  apt-get update
  apt-get install -y python-tk
  apt-get install -y libsm6 libxext6
  apt-get install -y libmagic-dev
  apt-get install -y libsndfile1
  pip3 install opencv-contrib-python
  pip3 install wrapt
  pip3 install pyyaml
  pip3 install joblib==0.11.0
  pip3 install librosa==0.5.0
  pip3 install pep8==1.7.0
  pip3 install nose==1.3.7
  pip3 install hyperopt
  pip3 install hyperas
  pip3 install tqdm
  pip3 install pyAudioAnalysis
  pip3 install hmmlearn
  pip3 install simplejson
  pip3 install eyed3
  pip3 install pydub
  pip3 install hyperas
  pip3 install webrtcvad
  pip3 install soundfile
  pip3 install ffmpeg-python
  pip3 install pyworld
  pip3 install autograd
  pip3 install pomegranate
  pip3 install crepe

%runscript
  # executes with the singularity run command
  # delete this section to use existing docker ENTRYPOINT command

%test
  # test that script is a success
