* Locally tested preparation steps:

Lab result URL
http://52.141.23.93:3000/sessions.html

## Containers and DevOps - Developer edition 
https://github.com/microsoft/MCW-Containers-and-DevOps/blob/master/Hands-on%20lab/HOL%20step-by-step%20-%20Containers%20and%20DevOps%20-%20Developer%20edition.md#exercise-1-create-and-run-a-docker-application

### Exercise 1: Create and run a Docker application

(Step 12 of Task 7)

## - Pre-requisites:
1. **Azure Subscription**
<pre>
  Azure 무료 계정 신청
  https://azure.microsoft.com/ko-kr/free/

  무료 계정 사용시 주의 사항
  https://docs.microsoft.com/ko-kr/azure/billing/billing-avoid-charges-free-account

  Azure 체험 계정은 처음 30일 동안 $200의 Azure 크레딧과 12개월 동안 무료 서비스라는 제한된 수량을 제공합니다.
  자세한 내용은 Azure 체험 계정을 참조하세요. 크레딧 상태에 따라 크레딧을 사용하거나 체험 서비스 및 수량을 초과한
  사용량에 대한 요금이 청구될 수 있습니다.
</pre>

2. **Create Ubuntu VM on Azure** :
 - Ubuntu 16.04 LTS
 - Extended OS Disk: 30GB -> 128GB

3. **Connect to VM using terminal emulator and install dependecy modules**:

<pre><code>
  curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
  sudo apt install docker.io mongodb-clients npm nodejs-legacy
  sudo npm install -g bower
  sudo curl -L https://github.com/docker/compose/releases/download/1.24.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
  sudo chmod +x /usr/local/bin/docker-compose
</code></pre>

4. **Make "source" directory under home folder and change directory to it** :

<pre><code>
  mkdir ~/source
  cd ~/source
</code></pre>

5. **Copy Lab file to local folder** :

<pre><code>
  curl -L -o FabMedical.tgz http://bit.ly/2uhZseT
</code></pre>

6. **Extract contents using following command** :

<pre><code>
  tar zxf FabMedical.tar.gz
</code></pre>

7. **Change directory to ~/source/FabMedical/content-init** :

<pre><code>
  cd ~/source/FabMedical/content-init
</code></pre>
