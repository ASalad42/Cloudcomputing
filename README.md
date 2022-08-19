<div align="center">

# Cloudcomputing
  </div>
  
 PowerPoint: 
https://testingcircle-my.sharepoint.com/:p:/g/personal/asalad_spartaglobal_com/Ecl94k_ny3dBm5tcw9AXx8IBQNQAkEwRAxKE8K4rIo8kUQ?e=RkzlUq
 
 Benifits 
 - cost effective
 - sacalbe
 - highly available 
 
 ![image](https://user-images.githubusercontent.com/104793540/185408317-24a0f52b-f2d7-48fe-8c82-36bee0733e22.png)


### On local host 

#### On AWS

<div align="center">
  
![image](https://user-images.githubusercontent.com/104793540/185448666-63595b2b-530c-439e-bb9a-483115eddc51.png)
![image](https://user-images.githubusercontent.com/104793540/185448828-8e82c3a2-74c3-43cb-9fd4-b314379849a2.png)
![image](https://user-images.githubusercontent.com/104793540/185448957-d5823f02-46a5-47ca-bbb7-8974d16c9f78.png)
![image](https://user-images.githubusercontent.com/104793540/185449268-b5bdbc89-100a-4492-984b-928f77816059.png)
![image](https://user-images.githubusercontent.com/104793540/185449416-5e55df12-27cc-4653-bfd7-ac43e1932491.png)
![image](https://user-images.githubusercontent.com/104793540/185449473-00a7ee80-6b8e-45bf-8927-e225cf9b9d1a.png)
![image](https://user-images.githubusercontent.com/104793540/185449540-1719ba44-196f-43bd-8133-2a125f4855c6.png)
![image](https://user-images.githubusercontent.com/104793540/185449680-eac82c52-9d6b-414d-a116-6f4ad38e186e.png)
Review and Launch 
 </div>
 
Then:
- Open an SSH client.
- /c/Users/Ayan/.ssh
- Locate your private key file. The key used to launch this instance is eng122.pem
- Run this command, if necessary, to ensure your key is not publicly viewable.
- `chmod 400 eng122.pem`
- Connect to your instance using its Public DNS:
- `ec2-52-213-75-136.eu-west-1.compute.amazonaws.com`
- ssh -i "eng122.pem" ubuntu@ec2-52-213-75-136.eu-west-1.compute.amazonaws.com

![image](https://user-images.githubusercontent.com/104793540/185450230-0cca1290-ec53-444e-9c8b-69ebd5751b58.png)
![image](https://user-images.githubusercontent.com/104793540/185450141-261c8cf1-2cf0-472e-9e00-5c430083b315.png)
![image](https://user-images.githubusercontent.com/104793540/185450021-42fdb86c-ce08-4ca9-8095-3eecee9f8e5d.png)

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

reverse proxy 
- cd /etc
- ls
- cd nginx
- cd sites-available
- sudo nano default
- proxy_pass http://localhost:3000;

![image](https://user-images.githubusercontent.com/104793540/185452344-3e82169d-37a1-4cd9-83c2-50418312055f.png)

- sudo nginx -t
- sudo systemctl restart nginx

![image](https://user-images.githubusercontent.com/104793540/185453023-57ca411a-a4ff-4b0a-993b-6af3a11cbc68.png)


![image](https://user-images.githubusercontent.com/104793540/185642911-a63e0b3f-da0e-4628-aa51-4a52cbe0dcd4.png)
