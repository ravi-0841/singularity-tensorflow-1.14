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
  pip install opencv-contrib-python
  pip install wrapt
  pip install pyyaml
  pip install joblib==0.11.0
  pip install librosa==0.5.0
  pip install pep8==1.7.0
  pip install nose==1.3.7
  pip install hyperopt
  pip install hyperas
  pip install tqdm
  pip install pyAudioAnalysis
  pip install hmmlearn
  pip install simplejson
  pip install eyed3
  pip install pydub
  pip install hyperas
  pip install webrtcvad
  pip install soundfile
  pip install ffmpeg-python
  pip install pyworld
  pip install autograd
  pip install pomegranate
  pip install crepe

%runscript
  # executes with the singularity run command
  # delete this section to use existing docker ENTRYPOINT command

%test
  # test that script is a success
