


### 1. Installing [Git](https://cloudaffaire.com/how-to-install-git-in-aws-ec2-instance/)

Create an EC2 instance with Amazon Linux 2 with internet access
Connect to your instance using putty
 
Perform a quick update on your instance:
```
sudo yum update -y
 ```

Install git in your EC2 instance
```
sudo yum install git -y
```

Check git version
```
git version
```

### 2. guide to install [zsh](https://blog.devops.dev/installing-zsh-oh-my-zsh-on-amazon-ec2-amazon-linux-2-ami-88b5fc83109) terminal

...

### 3. Installing [NVM](https://tecadmin.net/install-nvm-on-amazon-linux/) (Node Version Manager)

Node Version Manager official team provides a shell script for the installation of NVM command line utility. 

Use the following commands to install NVM on Amazon Linux system:

```
sudo yum install curl -y 
```
- download and install

> bash
```
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash   
```

or
>zsh
```
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash   
```
- associate 
```sh
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```



