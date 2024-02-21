# Introduction
As part of our studies at Octopus, I've developed a Python Utility Script for backing up files from the .conf file. Additionally, I've packaged it into an RPM package and made it available through nginx. To follow along with the guide, please refer to our blog post: [Packaging Your Python Script into a Custom Repository](https://rhel.co.il/2024/02/21/packaging-your-python-script-into-a-custom-repository/)

## 1. Update Repository Configurations 
To begin, update the repository configurations to include the SB Backup repository. Run the following command in your terminal:
```
sudo tee /etc/yum.repos.d/sb-backup.repo > /dev/null <<EOF
[sb-backup]
name=SB Backup Repository
baseurl=http://ip:port/repos
enabled=1
gpgcheck=0
EOF
```
This command downloads the repository configuration file and saves it as sb-backup.repo in the /etc/yum.repos.d/ directory.

## 2. Install the Package
Once the repository configuration is updated, install the package using the following command:

```
sudo dnf install sb-backup
```
This command installs the SB Backup package from the configured repository.

