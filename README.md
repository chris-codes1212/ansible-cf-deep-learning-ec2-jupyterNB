# ansible-cf-deep-learning-ec2-jupyterNB

## Description
Was in need of a server that I could run small deep learning projects on with a jupyter notebook service running to connect to locally. Due to the costs of the GPU machines in AWS (ie. g5 series ec2 instances), and the smaller needs at this time, I decided to use a cpu instance that was optimized for running smaller deep learning models (the c5 instance type seemed to fit the bill). 

The ansible playbook (dl_playbook) is designed to launch the cloudformation stack which creates the instance and the security group for ssh access and opens port 8888 (the default jupyter notebook service port). The notebook then waits for the instance to launch, and then configures by installing tensorflow and jupyter notebook as well as taking care of a few jupyter notebook configuration steps and starting jupyter notebook as a background service. 

This server allows me to ssh tunnel locally to it and then access the jupyter notebook by visiting http://localhost:8888.
