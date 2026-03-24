# CI/CD with Jenkins (Docker Setup)
<p align="center"> <img src="https://img.shields.io/badge/-Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white" /> <img src="https://img.shields.io/badge/-Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" /> <img src="https://img.shields.io/badge/-CI/CD-0A66C2?style=for-the-badge&logo=githubactions&logoColor=white" /> <img src="https://img.shields.io/badge/-Automation-FF6F00?style=for-the-badge&logo=automation&logoColor=white" /> <img src="https://img.shields.io/badge/-Linux-000000?style=for-the-badge&logo=linux&logoColor=white" /> <img src="https://img.shields.io/badge/-DevOps-0DB7ED?style=for-the-badge&logo=devops&logoColor=white" /> </p>

1. Run Jenkins in Docker
```
docker run -d \
  --name jenkins \
  --restart unless-stopped \
  -p 8080:8080 \
  -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  -e TZ=Asia/Kolkata \
  jenkins/jenkins:lts

```
2. Verify Container

```
docker ps
```
3. Access Jenkins Container

```
docker exec -it jenkins bash
```
4. Customize Terminal (Optional)

```
echo 'export PS1="\[\e[1;32m\]\u@\h\[\e[0m\]:\[\e[1;34m\]\w\[\e[0m\]\$ "' >> ~/.bashrc
```
5. Get Initial Admin Password

```
cat /var/jenkins_home/secrets/initialAdminPassword
```
