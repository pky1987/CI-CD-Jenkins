# CI/CD-Jenkins

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
