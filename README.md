## 1. Update Repository Configurations 
Update the repository configuration to include the SB Backup repository. Run the following command:
```
sudo tee /etc/yum.repos.d/sb-backup.repo > /dev/null <<EOF
[sb-backup]
name=SB Backup Repository
baseurl=http://172.29.159.12/repos
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

