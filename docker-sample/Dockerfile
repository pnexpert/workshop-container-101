FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
COPY BlazorApp /sources/BlazorApp
WORKDIR /sources/BlazorApp
RUN dotnet restore
RUN dotnet publish -c debug -o /app --no-restore

FROM mcr.microsoft.com/dotnet/aspnet:5.0
WORKDIR /app
COPY --from=build /app ./
EXPOSE 80
ENTRYPOINT ["dotnet","BlazorApp.dll"]
