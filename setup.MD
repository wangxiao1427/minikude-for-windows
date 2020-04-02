#### 以下用到了windows的包管理器Chocolatey，所以需要提前安装Chocolatey  
1. 使用管理员身份打开PowerShell，执行命令```Get-ExecutionPolicy```，确保Get-ExecutionPolicy不受限制。建议使用Bypass绕过策略来安装东西或AllSigned提高安全性。   
如果返回```Restricted```，则执行```Set-ExecutionPolicy AllSigned```或```Set-ExecutionPolicy Bypass -Scope Process```
2. 之后执行:  
```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))```
3. 执行完之后检查是否安装成功，输入```choco```
以上为choco命令的安装步骤  

## 正题
1. 安装docker for windows   
```choco install docker-for-windows -y```   
2. 安装minikube  
```choco install minikube -y```
安装完成之后搜索minikube:  
```
  PS C:\WINDOWS\system32> choco find minikube
  Chocolatey v0.10.15
  Minikube 1.9.0 [Approved]
  vscode-kubernetes-tools 1.1.1 [Approved]
  minishift 1.34.2 [Approved]
  kubeless 1.0.6 [Approved]
```

安装New-VMSwitch -Name "minikube" -AllowManagement $TRUE -NetAdapternmae "adapter名称"  
失败(待续...)
