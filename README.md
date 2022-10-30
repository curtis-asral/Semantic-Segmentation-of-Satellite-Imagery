# Semantic-Segmentation-of-Satellite-Imagery
How to Open NNI’s Web UI on Google Colab <br>
Install required packages and softwares.

! pip install nni # install nni <br>
! wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip # download ngrok and unzip it <br>
! unzip ngrok-stable-linux-amd64.zip <br>
! mkdir -p nni_repo <br>
! git clone https://github.com/microsoft/nni.git nni_repo/nni # clone NNI's offical repo to get examples <br>
Register a ngrok account here, then connect to your account using your authtoken. <br>

! ./ngrok authtoken YOUR_AUTH_TOKEN <br>
Start an NNI example on a port bigger than 1024, then start ngrok with the same port. If you want to use gpu, make sure gpuNum >= 1 in config.yml. Use get_ipython() to start ngrok since it will be stuck if you use ! ngrok http 5000 &. <br>

! nnictl create --config nni_repo/nni/examples/trials/mnist-pytorch/config.yml --port 5000 & <br>
get_ipython().system_raw('./ngrok http 5000 &') <br>
Check the public url. <br>

! curl -s http://localhost:4040/api/tunnels # don't change the port number 4040 <br>
You will see an url like http://xxxx.ngrok.io after step 4, open this url and you will find NNI’s Web UI. Have fun :) <br>

![Screenshot (90)](https://user-images.githubusercontent.com/94308793/198894113-905a0228-401b-45f8-9868-9425f5b7c3be.png)
