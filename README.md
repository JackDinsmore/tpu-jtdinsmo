# tpu-jtdinsmo

Created on 6/14/19 to store all of Jack Dinsmore's code for his 2019 summer UROP

ULTIMATE GOAL: analyze runtime of Resnet-50 and other algorithms on TPUs.


In order to run this code on Google Cloud, execute the following commands:

ssh -i <SSH FILE> -L localhost:9999:localhost:9999 <USER NAME>@<VM EXTERNAL IP>
jupyter notebook --ip 127.0.0.1 --port 9999 --no-browser
  
where SSH FILE is your local private key, USER NAME is your username for your ssh key on google cloud, and VM EXTERNAL IP is the ip address next to your VM, under the heading External IP in the Compute Engine/VM Instances page of google cloud. This notebook was run on the vm jtdinsmo-gpu.
