FROM adoptopenjdk/openjdk11

COPY /build/libs/schoolLetter-0.0.1-SNAPSHOT.jar /schoolLetter-0.0.1-SNAPSHOT.jar

EXPOSE 8080

# 실행 권한 추가
RUN chmod +x /schoolLetter-0.0.1-SNAPSHOT.jar

ENTRYPOINT ["java", "-jar", "/schoolLetter-0.0.1-SNAPSHOT.jar"]