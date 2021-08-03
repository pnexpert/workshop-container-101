# Dockerfile 的注意事項/技巧
這個資料夾裡包含一些撰寫 Dockerfile 的注意事項。  
docker build 的範例指令都寫在各個 Dockerfile 裡，執行指令的目錄是在這份文件的上層目錄，也就是 `workshop-container-101`。以下是一個範例，利用 `1-dockerignore` 裡的 Dockerfile 執行 docker build

```
PS C:\workshop-container-101> docker build -t aspnet-demo:dockerignore -f dockerfile-tips/1-dockerignore/Dockerfile ./dotnet-core-docker
```