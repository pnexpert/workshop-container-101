# 下載工作坊中使用的 Sample project
您可以選擇直接下載這份 repo 成為一個 `.zip` 檔案到您的工作機內

# 準備你的工作坊 Hands-on 環境
本工作坊的 Hands-on 課程需要您準備可執行 Docker 服務的系統，您可以選用 Windows 10, Mac 或是 Linux Kernel 4.5 以上版本的各種發佈版本 (CentOS, Ubuntu, Fedora 或是 Debian)。

Windows 與 Mac 的機器，[可以到這裡下載 Docker Desktop](https://www.docker.com/products/docker-desktop)  
CentOS 作業系統[可參考官方文件安裝](https://docs.docker.com/engine/install/centos/)  
Ubuntu 作業系統[可參考官方文件安裝](https://docs.docker.com/engine/install/ubuntu/)  
Fedora 作業系統[可參考官方文件安裝](https://docs.docker.com/engine/install/fedora/)  
Debian 作業系統[可參考官方文件安裝](https://docs.docker.com/engine/install/debian/)

# Windows 10 環境設置建議 
本工作坊的實作課程需要 Windows 環境的夥伴啟用 WSL2，這是一個由微軟自行編譯可在 Windows 10 作業系統中執行的 Linux kernel，可讓 Docker 在 Windows 中執行由 Linux kernel 封裝的容器應用。 在安裝 Docker Desktop for Windows 之前，請務必確認已經啟用 WSL2 與安裝相關的 Patch，相關的說明可以在下面第一點的 Docker 官方 WSL2 環境安裝提醒中獲得更多資訊：

* [請確認您的環境是否達到安裝 WSL2 的標準](https://docs.docker.com/docker-for-windows/wsl/#prerequisites)  
* [依照微軟官方文件步驟安裝 WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
* [下載和安裝 WSL2 的 Linux kernel 更新包](https://docs.microsoft.com/en-us/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package)
* [安裝 Docker Desktop 時啟用 WSL2](https://docs.docker.com/docker-for-windows/wsl/#install) 

* 安裝完成重新開機後，請在系統列對 docker 的圖示按一下滑鼠右鍵，選擇 Switch to Linux Container  
![switch](https://i.stack.imgur.com/96opa.png)
 
