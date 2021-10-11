# ipa_scripts

        curl -v  \
         -H referer:https://ipa.demo1.freeipa.org/ipa \
         -H "Content-Type:application/json" \
         -H "Accept:applicaton/json"\
         --negotiate -u : \
         --cacert /etc/ipa/ca.crt  \
         -d  '{"method":"user_find","params":[[""],{}],"id":0}' \
         -X POST https://ipa.demo1.freeipa.org/ipa/json

```Dockerfile
  FROM openjdk:8-jdk-alpine
WORKDIR /zookeeper/
COPY . /zookeeper/
RUN curl -O https://dlcdn.apache.org/maven/maven-3/3.8.3/binaries/apache-maven-3.8.3-bin.tar.gz && tar xzvf apache-maven-3.8.3-bin.tar.gz
CMD ["pipenv", "run", "python", "server.py"] 
