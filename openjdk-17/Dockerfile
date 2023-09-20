FROM alpine:3.17

# #******************更换Alpine源为mirrors.ustc.edu.cn******************
# RUN echo https://mirrors.ustc.edu.cn/alpine/v3.17/main > /etc/apk/repositories && \
#     echo https://mirrors.ustc.edu.cn/alpine/v3.17/community >> /etc/apk/repositories

#******************更换Alpine源为mirrors.nju.edu.cn******************
RUN echo https://mirrors.nju.edu.cn/alpine/v3.17/main > /etc/apk/repositories && \
    echo https://mirrors.nju.edu.cn/alpine/v3.17/community >> /etc/apk/repositories

RUN apk update && \
    apk add --no-cache openjdk17 openjdk17-jdk openjdk17-jmods openjdk17-demos openjdk17-doc openjdk17-jre-headless openjdk17-jre java-common java-cacerts \
    font-adobe-100dpi ttf-dejavu fontconfig \
    busybox libmcrypt libmcrypt-dev curl git make openssh-client autoconf supervisor tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone 