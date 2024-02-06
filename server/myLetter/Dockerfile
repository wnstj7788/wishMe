FROM adoptopenjdk/openjdk11

COPY /build/libs/myLetter-0.0.1-SNAPSHOT.jar /myLetter-0.0.1-SNAPSHOT.jar

EXPOSE 9997

# 실행 권한 추가
RUN chmod +x /myLetter-0.0.1-SNAPSHOT.jar

ENTRYPOINT ["java", "-jar", "/myLetter-0.0.1-SNAPSHOT.jar"]