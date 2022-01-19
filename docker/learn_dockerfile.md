# Dockerfile
https://docs.docker.com/engine/reference/builder/

## simple Dockerfile
```
FROM microsoft/dotnet:2.2-sdk AS builder
WORKDIR /app

COPY . .
RUN dotnet restore
RUN dotnet publish --output /out/ --configuration Release

EXPOSE 80
ENTRYPOINT ["dotnet", "aspnet-core.dll"]
```
## Multi-Stage Dockerfiles
```
FROM microsoft/dotnet:2.2-sdk AS builder
WORKDIR /app

COPY *.csproj  .
RUN dotnet restore

COPY . .
RUN dotnet publish --output /out/ --configuration Release

FROM microsoft/dotnet:2.2-aspnetcore-runtime-alpine
WORKDIR /app
COPY --from=builder /out .
EXPOSE 80
ENTRYPOINT ["dotnet", "aspnet-core.dll"]
```