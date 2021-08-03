# docker build -t aspnet-demo:multi-stage -f dockerfile-tips/4-multi-stage/Dockerfile ./dotnet-core-docker
FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine AS build

# copy csproj file first for restoring nuget package only
COPY BlazorApp/BlazorApp.csproj /sources/BlazorApp.csproj
WORKDIR /sources
RUN dotnet restore

# publish application
COPY BlazorApp/ /sources
# notice: the publish path is changed
RUN dotnet publish -c release -o /publish --no-restore
### end of build ###

# Build runtime image
FROM mcr.microsoft.com/dotnet/aspnet:5.0-alpine AS main
WORKDIR /app
COPY --from=build /publish .
ENV ASPNETCORE_URLS=http://+:80
EXPOSE 80
ENTRYPOINT ["dotnet", "BlazorApp.dll"]

# # check the image size:
# docker images

# # run this app:
# docker run -ti -p 8080:80 --rm aspnet-demo:multi-stage