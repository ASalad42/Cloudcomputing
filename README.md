<div align="center">

# Cloudcomputing
  </div>
 
 Benifits 
 - cost effective
 - sacalbe
 - highly available 
 
 ![image](https://user-images.githubusercontent.com/104793540/185408317-24a0f52b-f2d7-48fe-8c82-36bee0733e22.png)


### On local host 
Start > connect >
- Open an SSH client.
- /c/Users/Ayan/.ssh
- Locate your private key file. The key used to launch this instance is eng122.pem
- Run this command, if necessary, to ensure your key is not publicly viewable.
- `chmod 400 eng122.pem`
- Connect to your instance using its Public DNS:
- `ec2-52-213-75-136.eu-west-1.compute.amazonaws.com`
- ssh -i "eng122.pem" ubuntu@ec2-52-213-75-136.eu-west-1.compute.amazonaws.com

### Inside VM
- `Uname –a` 
- `pwd`
- `sudo apt-get update`
- `sudo apt-get upgrade`
- `sudo apt install nginx –y`
- `systemctl nginx status`
- Public IP address in ec2 instance connect

![image](https://user-images.githubusercontent.com/104793540/185434066-7a031485-3666-498d-8781-1409d624a3d2.png)
![image](https://user-images.githubusercontent.com/104793540/185434946-10aec777-ae1b-411c-9537-5a3c545dd974.png)


- `sudo apt-get install -y nodejs`
- `curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -`
- `sudo apt-get install -y nodejs`

- App is on local host > copy to ec2 

- ![image](https://user-images.githubusercontent.com/104793540/185432100-73946bb0-7174-4c00-b537-71c1b2a7988b.png)

- `scp  -i ~/.ssh/eng122.pem -r /c/Users/Ayan/aws ubuntu@ec2-52-213-75-136.eu-west-1.compute.amazonaws.com:`


- `cd app`
- `sudo apt install npm`
- `npm start`

![image](https://user-images.githubusercontent.com/104793540/185433908-f60bd2f3-e64b-4d61-8540-2bcd7d6852bf.png)

- edit security group to add another rule to allow port 3000 to all

![image](https://user-images.githubusercontent.com/104793540/185447994-e37a2989-6ef7-46ce-a329-65339f2e7204.png)

![image](https://user-images.githubusercontent.com/104793540/185448188-c5bc53d3-d835-413e-9b70-8c17c682172f.png)

![image](https://user-images.githubusercontent.com/104793540/185448262-a3b10648-30c3-4e1e-8fa8-b28c2d2956ef.png)

