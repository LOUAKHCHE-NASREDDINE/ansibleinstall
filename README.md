# ansibleinstall
The following shell script downloads and installs the current preview release of PowerShell. You can change the URL to download the version of PowerShell that you want to install
###################################
# Prerequisites

# Update the list of packages
sudo apt-get update

# Install pre-requisite packages.
sudo apt-get install -y wget

# Download the PowerShell package file
wget https://github.com/PowerShell/PowerShell/releases/download/v7.4.6/powershell_7.4.6-1.deb_amd64.deb

###################################
# Install the PowerShell package
sudo dpkg -i powershell_7.4.6-1.deb_amd64.deb

# Resolve missing dependencies and finish the install (if necessary)
sudo apt-get install -f

# Delete the downloaded package file
rm powershell_7.4.6-1.deb_amd64.deb

# Start PowerShell Preview
pwsh
