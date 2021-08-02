
### 使用 powershell.exe 安装

使用 PowerShell，您必须确保Get-ExecutionPolicy不受限制。我们建议使用Bypass绕过策略来安装东西或AllSigned提高安全性。

运行Get-ExecutionPolicy。如果它返回Restricted，则运行Set-ExecutionPolicy AllSigned或Set-ExecutionPolicy Bypass -Scope Process。

现在运行以下命令：

  Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

将复制的文本粘贴到 shell 中，然后按 Enter。

### Chocolatey的使用

choco search <keyword>    //搜索软件
  
choco list <keyword>  //跟 search 命令功能类似
  
choco install <package1 package2 package3...>  //安装软件
  
choco install <package>  -version *** //安装指定版本
  
choco  uninstall name //卸载软件
  
choco version <package>  //查看安装包的版本情况
  
choco  upgrade <package>   //更新某个软件 
  
choco list -localonly        //查看一下所有安装在本地的包的列表
  
choco list -lo       //功能同上
  
