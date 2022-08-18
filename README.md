<div align="center">

# Cloudcomputing
  </div>
 
 Benifits 
 cost effective, sacalbe, highly available 
 
 ![image](https://user-images.githubusercontent.com/104793540/185408317-24a0f52b-f2d7-48fe-8c82-36bee0733e22.png)


- OS windows10/11 - ubuntu bionic16.04LTS - vagrant box online 
- Process power 
- Ram 
- SSD - storage - volume - persistent data (as USB/Pen drive - comes with cost) > 
- hard drive 
- graphic card 
- power supply 
- cpu
- motherboard - poor quality - led to problems - eventually needed to replace it 
- touch screen
- upgrading RAM? to increase performance 
- Firewall - secruity tool 
- good quality - ready to pay the price for good quality 
- purpose: personal use, work, gaming 


Start > connect >
- Open an SSH client.
- /c/Users/Ayan/.ssh
- Locate your private key file. The key used to launch this instance is eng122.pem
- Run this command, if necessary, to ensure your key is not publicly viewable.
- `chmod 400 eng122.pem`
- Connect to your instance using its Public DNS:
- `ec2-52-213-75-136.eu-west-1.compute.amazonaws.com`
- ssh -i "eng122.pem" ubuntu@ec2-52-213-75-136.eu-west-1.compute.amazonaws.com

`Uname –a` 
`pwd`
`sudo apt-get update`
`sudo apt-get upgrade`
`sudo apt install nginx –y`
`systemctl nginx status`

- Public IP address in ec2 instance connect

`sudo apt-get install -y nodejs`
`curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -`
`sudo apt-get install -y nodejs`

- App is on local host > copy to ec2 
-
- ![image](https://user-images.githubusercontent.com/104793540/185432100-73946bb0-7174-4c00-b537-71c1b2a7988b.png)

`scp  -i ~/.ssh/eng122.pem -r /c/Users/Ayan/aws ubuntu@ec2-52-213-75-136.eu-west-1.compute.amazonaws.com:`
