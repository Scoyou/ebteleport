# AWS Elastic Beanstalk Tool
This is a CLI tool to SSH into an AWS E2 Instance or open the EB environment for the instance in the browser
supports vim style key presses

For use with Bridge custom dev EB environments

# Usage
Clone repo
```
git clone git@github.com:Skezey/aws-cli-tool.git
cd aws-cli-tool
```
Make ebteleport script executable
```chmod +x ./ebteleport```

Move script to path, IE: ```cp ./ebteleport /usr/local/bin/```

Run script by typing ```ebteleport```

# Dependencies
This script assumes you have the AWS EB CLI already installed. If not, see [installation instructions](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)

It also assumes you have configured your Bridge AWS credentials with [AWS-Vault](https://github.com/99designs/aws-vault)

ebteleport relies on the following gems:
* [tty-prompt](https://github.com/piotrmurach/tty-prompt)
* [launchy](https://github.com/copiousfreetime/launchy)
* [JSON](https://github.com/flori/json)

All required gems will be installed automatically when the script is first ran
