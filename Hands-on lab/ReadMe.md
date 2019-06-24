* Locally tested preparation steps:

## Containers and DevOps - Developer edition 
https://github.com/microsoft/MCW-Containers-and-DevOps/blob/master/Hands-on%20lab/HOL%20step-by-step%20-%20Containers%20and%20DevOps%20-%20Developer%20edition.md#exercise-1-create-and-run-a-docker-application

### Exercise 1: Create and run a Docker application

(Step 12 of Task 7)

## - Pre-requisites:
1. **Azure Subscription**

2. **Create Ubuntu VM on Azure** :
 - Ubuntu 16.04 LTS
 - Extended OS Disk: 30GB -> 128GB

3. **Connect to VM using terminal emulator and install dependecy modules**:

<pre><code>
  curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
  sudo apt install docker.io mongodb-clients npm nodejs-legacy
  sudo npm install -g bower
  curl -L https://github.com/docker/compose/releases/download/1.24.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
  chmod +x /usr/local/bin/docker-compose
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
  tar ztvf FabMedical.tar.gz
</code></pre>

7. **Change directory to ~/source/FabMedical/content-init** :

<pre><code>
  cd ~/source/FabMedical/content-init
</code></pre>
