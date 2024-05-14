FROM mcr.microsoft.com/dotnet/sdk:8.0-alpine
COPY src /app
WORKDIR /app
RUN ["dotnet", "restore"]
RUN ["dotnet", "build", "--configuration", "Debug"]
EXPOSE 5000/tcp
ENV ASPNETCORE_URLS https://*:5000
ENTRYPOINT ["dotnet", "run", "--server.urls", "http://*:5000"]