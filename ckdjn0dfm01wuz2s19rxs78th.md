## How to setup SSH for Github in Linux?


The developer's most used tool was Github, so every time you push your changes you will be asked to enter your Github details which is a tiresome work so setting an ssh key to your Github will make your life a lot easier.  
## Through the following commands you can easily setup ssh for GitHub in Linux 

* Open Your terminal and set the following 
```
git config --global user.name 'Your GitHub username'
git config --global user.email 'your GitHub associated email'
``` 

* After this step check if you have any SSH keys present locally by this commad.
```
ls ~/.ssh
``` 

* Now you have to generate ssh key in your terminal with the following command and click as enter for all the options as default values willl be enough for creating a ssh key
```
ssh -keygen -t rsa -b 4096 -c 'your Github associated email address'
```

* Now you have to copy the ssh and paste it in your github ssh settings, we can copy the ssh key easily using xclip.

* First install XCLIP through the following command
```
sudo apt-get install xclip
```

* Now copy your ssh key using xclip by this command
```
xclip -sel clip < ~/.ssh/id_rsa.pub
```

* Now open your GitHub account in the browser go to settings and select SSH and GPG Keys from the left sidebar.
![Screenshot from 2020-08-07 07-47-32.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1596766675006/zuH9s3hjb.png)

* Now Click New SSH Key button.
![Screenshot from 2020-08-07 07-49-15.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1596768728320/ttHDQE0U1.png)

* Now enter Your title and enter the copied ssh key from earlier. 

![Screenshot from 2020-08-07 07-49-47.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1596766804138/cu6uDDZyr.png)

* Now open your terminal and Check the ssh key using this command.
```
ssh -T git@github.com
```
* After this, you will be prompted with this text 
```
Hi Username! You've successfully authenticated, but Github does not support shell access. 
```

### Refernce 

If you are struck anywhere, please refer to this video tutorial https://www.youtube.com/watch?v=HfTXHrWMGVY.

### Conclusion 

Please try to use SSH for GitHub as it makes a life a lot easier and secure. If you are struck anywhere feel free to comment below I can help you to set up or some can help with your problem.


















