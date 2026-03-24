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
```
docker ps
```

```
docker exec -it jenkins bash
```

```
echo 'export PS1="\[\e[1;32m\]\u@\h\[\e[0m\]:\[\e[1;34m\]\w\[\e[0m\]\$ "' >> ~/.bashrc
```

```
cat /var/jenkins_home/secrets/initialAdminPassword
```
