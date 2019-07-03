
*** TensorBoard Jupyter Notebook ***

$ docker run -it -p 8888:8888 -p 6006-6015:6006-6015 16ba41f5406d
Jupyter Notebook : http://localhost:8888 


$ docker ps -a
CONTAINER ID        IMAGE                             COMMAND                  CREATED             STATUS                     PORTS                                            NAMES
a84c46c4b7cc        16ba41f5406d                      "bash -c 'source /..."   About an hour ago   Up About an hour           0.0.0.0:6007->6007/tcp, 0.0.0.0:8888->8888/tcp   frosty_brahmagupta

$ docker run -it -p 8888:8888 -p 6006-6015:6006-6015 tensorflow/nightly-py3-jupyter
$ docker commit a84c46c4b7cc tensorflow/nightly-py3-jupyter-v1.0
$ docker exec -it a84c46c4b7cc /bin/bash
$ docker start/stop/rm a84c46c4b7cc

[docker tag local-image:tagname new-repo:tagname]
$ docker tag tensorflow/nightly-py3-jupyter-v1.0:latest isunyoo/tensorflow:nightly-py3-jupyter-v1.0
$ docker rmi <old_name> #Remove the old tag

$ docker login
 Username: isunyoo
 Password: ~~~

[docker push new-repo:tagname]
$ docker push isunyoo/tensorflow:nightly-py3-jupyter-v1.0
$ docker pull isunyoo/tensorflow:nightly-py3-jupyter-v1.0

$ docker images
$ docker image remove 6d98596f7e50
$ docker rmi -f 376bbda9a165


$ docker rename 9c44048e4154 tensorflow-nightly-py3-jupyter
[syoo@localhost ~]$ docker ps -a
CONTAINER ID        IMAGE                             COMMAND                  CREATED             STATUS                     PORTS                                            NAMES
9c44048e4154        16ba41f5406d                      "bash -c 'source /..."   20 hours ago        Up 13 minutes              0.0.0.0:6007->6007/tcp, 0.0.0.0:8888->8888/tcp   tensorflow-nightly-py3-jupyter


*** TensorBoard Docker Image ***

$ docker run -it -p 6006:6006 tensorflow/tensorflow:nightly-py3-jupyter
TensorBoard : http://localhost:6006/



