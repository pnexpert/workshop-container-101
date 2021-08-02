FROM mcr.microsoft.com/dotnet/sdk:5.0
COPY BlazorApp /sources/BlazorApp
WORKDIR /sources/BlazorApp
RUN dotnet restore
RUN dotnet publish -c release -o /app --no-restore
WORKDIR /app
ENV ASPNETCORE_URLS=http://+:80
EXPOSE 80
ENTRYPOINT ["dotnet","BlazorApp.dll"]
