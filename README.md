# Flask Docker App

This is a simple Flask application designed to be dockerized in later lessons.

Containerizing a Flask App with Docker

A modular Flask web application built step-by-step for local and Dockerized environments.

Step: 1  Build a Basic Flask App:
 Create a Basic Flask Application
Project File Structure

flask_docker_app/
├── app/
│   └── main.py
├── requirements.txt
└── README.md

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/f89dc05f-c0d6-426b-adfe-b4221eb04da2" />

Create main.py inside the app/ folder
Main.py:
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/bb2416b8-29f9-438c-bb6e-bfc4c29fed21" />

Step 2: Create requirements.txt in the root
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/4ad93f59-e451-4268-938c-076f29d13ed6" />

Step 3: (Optional) Create a README.md
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/41ff7ad2-6e24-420b-8704-681274e895a1" />

Step 4: Run the Flask App Locally
# Navigate to project directory
cd flask_docker_app

# Create virtual environment (optional but recommended)
python3 -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/4f9e3c9c-9304-4cc3-bde5-7617f803e6fc" />


# Install dependencies
pip install -r requirements.txt
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/90183871-b092-4a20-9f8b-eefd2ba8f1bf" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/5568a9aa-1b8a-4958-ad92-ba32db3227a3" />


# Run the app
python app/main.py
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/5f8d4866-ec7a-4f00-802b-fc74b9730320" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/b255bd31-6467-472a-8053-49dcd82428d0" />

Setting up an ubuntu aws instance:
Name : ubuntuServer
AMI : Ubuntu 24.04 LTS
Instance type : t2 micro
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/0092f694-d229-4b15-ae26-a7d3178ff7f2" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/8519e81b-7253-441c-8635-ee0c78fe0e98" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/2a66fd6c-52f0-41d2-8e28-209f5a753708" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/f045f6e4-2ac3-44bc-949a-02180fc28ea5" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/98908a8e-5d7d-4f30-a0e6-0aff7f1a8b2d" />

Connecting ubuntuServer using InstanConnect:
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/8abbc7cc-8425-4d25-993b-2c3972d2abac" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/51f6cbf2-11d0-49db-a328-c08bf3ed8036" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/3aa9ea2e-ad39-4ff0-9199-0248773a82e2" />

Update the System
Sudo apt update –y
Sudo apt upgrade –y
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/3a7eaf8c-887a-432c-a19b-d8caba6753fd" />
Install Prerequisites
sudo apt install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common \
    gnupg \
    lsb-release -y
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/cc7f9e08-5301-45f0-8d54-534d4e7d78b0" />


Add Docker's Official GPG Key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
  sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/4332b2dd-d86c-4c9f-9ae2-fa9b08d3cfa3" />

Set Up the Docker Repository
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null


  <img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/b1c605a0-df49-4579-9c3d-76ddb1fc8e75" />

   Install Docker
   sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io –y

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/eee2e17f-bdd6-4f7f-b353-3d1fb2776a72" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/7b5c84c8-0ecd-4a84-96ef-35765cca3ddb" />

Add Your User to the Docker Group
sudo usermod -aG docker $USER
newgrp docker

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/a9478843-f153-4e44-9f1f-52bd3a6005e5" />

Enable and Start Docker
sudo systemctl enable docker
sudo systemctl start docker

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/857c7e5e-6265-45ec-af28-b337728bc209" />

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/7c6176b6-02ab-4d08-a5ca-db083680aa97" />

Test Docker
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/7b7b2fdd-63dc-437b-baa3-19134b7a6a57" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/e0e3dc4d-62eb-48f8-a67a-ae8d8a73b0ec" />

Create Dockerfile in the Root
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/e1043088-bbcf-4a37-802f-0037e78bea2d" />
Create .dockerignore
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/389e6c10-305e-4857-9af5-570724ef11b5" />

Transferring project to github repository:
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/07bb6f6b-a20f-432f-a95a-9f7183bd1b38" />

Cloning the repo into ubuntuServer ec2 instance
Git clone https://github.com/saiyedin786/python-flask-app.git

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/88c512cb-c996-4ba3-8c59-18e57c921f68" />

Cd into python_flask_app folder;
Buiding image:
docker build -t flask-docker-app .
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/835101ee-858d-49bf-ac69-c4186b394a2e" />


Docker images:
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/246d1f43-2219-4f15-a197-ecc3c5f03162" />

Running container from the image:
docker run -p 5000:5000 flask-docker-app
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/104551d6-f078-46fe-90f1-b11a658cc318" />

Testing in browser:
Allowing 5000 port in security group of ec2 instance
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/9bda06d5-3d33-4324-8724-c6ad77eff210" />
url : http://3.90.26.44:5000/
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/cb2c7a1c-98f6-4a32-bf92-8e9289e34deb" />

Configuring ci cd pipeline using github actions:
Creating deply.yml file 
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/914f7b4a-55a4-46c8-8d54-50a4200fb7a2" />

Writing code for yml file:
name: Deploy flast app to EC2
on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repo
        uses: actions/checkout@v3
        
      - name: Deleting content on ec2
        uses: appleboy/ssh-action@v1.0.3
        with:
          host: ${{ secrets.EC2_HOST }}
          username: ${{ secrets.EC2_USER }}
          key: ${{ secrets.EC2_SSH_KEY }}
          script: |
            cd ~
            sudo rm -rf *
            

      - name: Copy files to EC2
        uses: appleboy/scp-action@v0.1.7
        with:
          host: ${{ secrets.EC2_HOST }}
          username: ${{ secrets.EC2_USER }}
          key: ${{ secrets.EC2_SSH_KEY }}
          source: "./*"
          target: "/home/${{ secrets.EC2_USER }}/python_flask_app"

      - name: creating docker image and running the container
        uses: appleboy/ssh-action@v1.0.3
        with:
          host: ${{ secrets.EC2_HOST }}
          username: ${{ secrets.EC2_USER }}
          key: ${{ secrets.EC2_SSH_KEY }}
          script: |
            sudo apt update
            cd python_flask_app
            docker build -t flask-docker-app .
            docker run -p 5000:5000 flask-docker-app

pasting this code into deploy.yml file
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/d47dbd94-0ac0-4ba9-bc2b-91c9eacf885c" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/973c8a14-eb4c-4009-976f-95515202d62f" />

And then saving the file

Setting secrets in github actions:
Settings->secrets and actions-> actions->New Repository secrets
Saving 3 secrets as:
1. EC2_USER - ubuntu
2. EC2_SSH_KEY – copy the content of key which downloaded from ec2 instance
3. EC2_HOST – ip of ec2 instance
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/2a495acf-307e-48ef-ac21-cae15254119f" />

Now when any changes will be made in local computer and is then pushed into github main repo than this deploy.yml will work. It will first login into ec2 instance and delete folder from /home/ubuntu/ directory, places updated folder and then creates a image and than runs container from the image

Making changes in the local computer code:
Adding templates/index.html and static/style.css in local git repo as follows
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/ce6a0984-4f61-4cc7-9908-0f56f786c6c3" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/19205bd1-c19b-482b-b81c-ab61b0174b55" />

Now making changes in app.py so as to render index.html template:
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/7a76e73a-fdec-490d-a1ec-909546d3208a" />

Now running following commands to push into github remote repo
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/45d1c617-5821-4f3e-ab67-92cb9f3ff65a" />

As soon as I pushed code into main branch ci cd worked and workflow executed
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/7b5bf7e0-f9f5-4984-b87d-c265ac0e9ef4" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/d24a5d32-1d5a-4ca0-a991-fb0d28289b97" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/76c5c737-f62c-49af-8e04-493765f48f2f" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/bb3162a7-7642-44e3-80d4-4c64bab47a4c" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/873ac681-12ed-487e-81f5-522049d2bc60" />

Using Environment variables:
Install python-dotenv
python-dotenv==1.0.1
Create the .env File

Update main.py to Use Environment Variables
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/328d8228-e0d0-4317-b53f-d84a5ae3dd91" />

Update .dockerignore to Exclude .env

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/9478f016-b840-4c3e-98d8-efd0054b825a" />

Push the code to github repo and then code will be deployed to ec2 automatically using github actions ci cd pipeline
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/1c1a6f37-71c7-4b62-a747-f9016f159ba5" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/cc290d34-bae9-472c-a4ac-0b1e9543b2f0" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/14bf93b2-057b-4488-ad6b-4c2524534fab" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/a270f1c0-fc3b-4738-a277-681edeffdf1d" />


Docker compose integration:
Updating index.html
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/fc37e9b5-7f7c-42ad-a45a-7800ffd06d47" />

Create result.html to Show Form Output
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/63717e4f-fb53-4e7f-a3e3-c57c7c90e2d1" />

Updating main.py
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/988d09d4-ecbf-48af-9f6c-949e3a87864a" />

Create docker-compose.yml
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/319e9b4d-8978-4a74-ae96-ce78e3ceac88" />

Pushing changes into github repo

Modifying deploy.yml into github actions
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/11554212-fda2-4fd3-9cd1-736bf5899268" />
Pushing data into github repo
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/f86a95b7-ff12-427c-9b27-9baf0e0d482f" />

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/88ee545e-fb78-4aa6-96e4-e10631934af8" />
<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/cb547a91-6604-42dc-a6cc-97d598e2da8c" />

Testing:
http://54.226.0.148/
![Uploading image.png…]()


































































