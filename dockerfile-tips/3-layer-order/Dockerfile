# docker build -t aspnet-demo:restore-first -f dockerfile-tips/3-layer-order/Dockerfile ./dotnet-core-docker
FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine

# copy csproj file first for restoring nuget package only
COPY BlazorApp/BlazorApp.csproj /sources/BlazorApp.csproj
WORKDIR /sources
RUN dotnet restore

# publish application
COPY BlazorApp/ /sources
RUN dotnet publish -c release -o /app --no-restore
WORKDIR /app

# run the app
ENV ASPNETCORE_URLS=http://+:80
EXPOSE 80
ENTRYPOINT [ "dotnet", "BlazorApp.dll" ]

# # run this app:
# docker run -ti -p 8080:80 --rm aspnet-demo:restore-first