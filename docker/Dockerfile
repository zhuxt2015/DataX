FROM yldc-docker.pkg.coding.yili.com/pubrepo/pubdocker/openjdk8_odps:1.0
# tag: openjdk8_322  openjdk11_0.14  openjdk8  openjdk11  openjdk16  oraclejre8u201
MAINTAINER by coding
# ENV LANG en_US.UTF-8 


# ---------------------只改此处，其它不动--------------------------
# 定义jar包文件名  当前目录 ./ 为代码根目录
# ARG JARFILE=./xxxx/xxx/target/xxxxx.jar
#ARG JARFILE=./target/datax/datax.tar.gz
# --------------------------------------------------------------------

# 定义appName=k8s服务名，外部传参
#ARG appName
#ENV appName ${appName}
#COPY --chown=ylapp   ${JARFILE}   /data/app/${appName}.tar.gz

#WORKDIR /data/app
USER ylapp
EXPOSE 8080
CMD ["sh", "-ec", "exec java ${JAVA_OPTS} -Dspring.profiles.active=${workEnv} -Dserver.port=8080 -Xshare:off -jar ${appName}.jar "]