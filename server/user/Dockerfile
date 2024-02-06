FROM adoptopenjdk/openjdk11

COPY /build/libs/user-0.0.1-SNAPSHOT.jar /user-0.0.1-SNAPSHOT.jar

EXPOSE 9998

# 실행 권한 추가
RUN chmod +x /user-0.0.1-SNAPSHOT.jar

ENTRYPOINT ["java", "-jar", "/user-0.0.1-SNAPSHOT.jar"]