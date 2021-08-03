# # run command in .\BlazorApp\ to generate complied files: dotnet run
# docker build -t aspnet-demo:dockerignore -f dockerfile-tips/1-dockerignore/Dockerfile ./dotnet-core-docker
FROM mcr.microsoft.com/dotnet/sdk:5.0

COPY BlazorApp /sources/BlazorApp

# # run the command below to see bin folder inside
# docker run -ti aspnet-demo:dockerignore ls /sources/BlazorApp/bin

# to ignore folder bin and obj, copy .dockerignore to parant path 
