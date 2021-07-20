編譯您的容器
```
docker build -t dotnet-core-docker .
```

執行您的容器，檢視完畢後使用後 Ctrl + C 組合鍵關閉容器。
```
docker run -it -p 80:80 --rm dotnet-core-docker
```

修正程式碼後，再次編譯您的容器，並加上 tag。  
編譯完成後，執行您剛剛編譯好的容器。
```
docker build -t dotnet-core-docker:20210730 .
docker run -it -p 80:80 --rm dotnet-core-docker:20210730
```

使用背景模式執行容器，為容器指定一個易於辨識的名稱。
```
docker run -d -p 80:80 --name dotnet-core-demo dotnet-core-docker:20210730
```