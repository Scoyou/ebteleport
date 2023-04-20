# Ebteleport
This is a CLI tool to SSH into an AWS E2 Instance or open the EB dashboard for the instance in the browser.
Supports vim style key presses.

For use with [Get Bridge](https://github.com/get-bridge) custom dev EB environments.

## Getting Started
Clone repo
```
git clone git@github.com:Skezey/ebteleport.git
cd ebteleport
```
Make ebteleport script executable
```chmod +x ./ebteleport```

Move executable to path, IE: ```cp ./ebteleport /usr/local/bin/```

Run script by typing ```ebteleport```

## Usage
Use arrow keys or vim's h-j-k-l to navigate CLI menu, press enter to make a selection:

![image](https://user-images.githubusercontent.com/36577381/143939750-45c3c9c7-a491-4391-a866-368b44c764f8.png)
![image](https://user-images.githubusercontent.com/36577381/143939818-61f8bb22-7ae0-4c1f-ad54-bcef649cf485.png)

While hovering over the desired environment, hit "enter" to be brought to a sub menu where you can select to SSH into the env or be brough to the AWS eb dashboard in your browser:

![image](https://user-images.githubusercontent.com/36577381/233450267-10558e83-f69a-4bfa-9076-8ed226b7971c.png)

Alternatively, you can type out the env you want to access as a command line arguement to directly SSH into the ec2 instance without going through the menus:
```bash
ebteleport bridge-custom-reports-staging
```

# Dependencies
This script assumes you have the AWS EB CLI already installed. If not, see [installation instructions](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html).

It also assumes you have configured your Bridge AWS credentials with [AWS-Vault](https://github.com/99designs/aws-vault).

ebteleport relies on the following gems:
* [tty-prompt](https://github.com/piotrmurach/tty-prompt)
* [launchy](https://github.com/copiousfreetime/launchy)
* [JSON](https://github.com/flori/json)

All required gems will be installed automatically when the script is first ran.
