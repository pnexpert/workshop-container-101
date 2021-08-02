# docker build -t aspnet-demo:alpine -f 2-base-images/alpine/Dockerfile .
FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine
COPY BlazorApp /sources/BlazorApp
WORKDIR /sources/BlazorApp
RUN dotnet restore
RUN dotnet publish -c release -o /app --no-restore
WORKDIR /app
ENV ASPNETCORE_URLS=http://+:80
EXPOSE 80
ENTRYPOINT ["dotnet","BlazorApp.dll"]

# # check the image size:
# docker images

# # check the function:
# docker run -ti -p 8080:80 --rm aspnet-demo:alpine