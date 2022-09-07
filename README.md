# BOTS-ShellCode
by this repo we realize How we can launch boss of the soc toolkit in local as splunk enterpize single instance and take an exam of our  SOC Team for incident response

if you google based on your threat Detection may you can find SPLUNK page on github 
and BoTs/v1/v2/v3 has DataSet for your examine as his guide Downlaod DataSet Attack Only for your Threat analysis. In my google if you want waste of your time
, Downloads each of add-on/Application and install manually or use Auto Shell code in bash/shell script. 
#### Notice: Trace each of line shell script, don't let curl compromise (Botnet Alert).

#### Official Splunk Boss Of The SOC DataSet
BOTS-v1 https://github.com/splunk/botsv1
BOTS-v2 https://github.com/splunk/botsv2
BoTs-v3 https://github.com/splunk/botsv3

### . BoTs-v3 -Installation Guide
For your Installation and use CTF challenge use this repo https://github.com/runasroot/BOTSv3_install based on this https://run-as-root.com/2021/06/08/splunk-botsv3-install-and-configuration/ article written in 2021. The install-botsv3.sh is better than installation of detection lab repo as following. I suggest Read and Take his
syntax to install your BoTsv2,v1 . See this Shell Script of DetectionLab and Realize Why run-as-root' shell is better than others https://github.com/clong/DetectionLab/blob/master/Vagrant/scripts/install-botsv3.sh .

### .BoTs-v2 -Installation Guide
Use this repo becareful what you see in his shell script don't be compromise as victim run this DataSet in your Isolate Network. https://github.com/clong/DetectionLab/blob/master/Vagrant/scripts/install-botsv2.sh

### .BoTs-v1 -Installation Guide 
We use just BoTs-v1 from SPlunk repo (DataSet Attack Only) by this  https://github.com/orgs/splunk/repositories?q=Bots&type=all&language=&sort=  for your installation 
use ran as root shell script syntax I push in this repo.

### Auto CheckSum Splunk Hash file using Powershell 

```
$HashString = Read-Host -Prompt "Enter Your Hash"
While ($true) {
    $Filepath = Read-Host -Prompt "Please enter a path of your add-on has downlaoded"
    if (Test-Path -Path $Filepath) {break}
    Write-Host "Wron path. PLZ try again" -ForegroundColor Red
}
$Filepath=(Get-FileHash $Filepath -Algorithm SHA256).Hash
if ($HashString -eq $Filepath) {Write-Host "Your Hash Files is The Same" -ForegroundColor green "\n" }
Elseif ($HashString -ne $Filepath){Write-Host "your hash files are not in the same" -ForegroundColor Red "\n" }
```
