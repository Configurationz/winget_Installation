# WinGet Installation on Windows 10 (x86)

### Follow this Guide to successfully install Winget on Windows 10 21H1 version any Edition _(Home, Pro, etc.)_


My set of commands to install Winget on Windows 10

* Open an elevated terminal and execute the below command
```
Invoke-WebRequest -Uri https://github.com/microsoft/winget-cli/releases/download/v1.8.1911/Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle -OutFile ~\Downloads\WinGet.msixbundle
```

* This will download the `msixbundle` file to your `~\Downloads` folder

* The latest version at the moment is `v1.8.1911`. The current, latest and other versions can be found on GitHub

* Ensure to download the latest bundle from here [^1]

* Next step
```
Add-AppxPackage ~\Downloads\WinGet.msixbundle
```

* Verify the installation
```
winget --version
```


Additionally, try the following steps if you're unable to download/install any available software from Microsoft Store

* Go to Microsoft Store and copy the link of the app you want to install from [Microsoft | Store](https://apps.microsoft.com/store/apps)

* Copy the link of the app and paste in this website "[Online link generator for Microsoft Store](https://store.rg-adguard.net)" and search in `RP` mode 

* In the result, find the `.appx` file of the app you need and right click and do save as, your browser might detect it as a harmful app, but you can ignore and download it

* Ensure you also download all the dependencies and save them as well

* Once you've downloaded all the dependencies and the application, start by installing dependencies first, and then the main application

* To install, go to the Downloads location, right click on each file and click `Install`

* Optional: you can also install via _powershell_
```
Add-AppxPackage -Path "<PATH of the file>".appx
```


## Troubleshooting

- [How do I get the Windows Package Manager?](https://github.com/microsoft/winget-cli/blob/master/doc/troubleshooting/README.md)

- [How to open Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.appxbundle? #347](https://github.com/microsoft/winget-cli/issues/347)

- [Install winget by the command line (powershell)](https://stackoverflow.com/questions/74166150/install-winget-by-the-command-line-powershell)

- [Windows Package Manager 1.2.10271](https://github.com/microsoft/winget-cli/releases/tag/v1.2.10271)


## References

* superuser - 
[It is possible to install microsoft app installer using the command line?](https://superuser.com/questions/1701930/it-is-possible-to-install-microsoft-app-installer-using-the-command-line)

* GitHub - 
[Windows Package Manager 1.9.2411-preview Pre-release](https://github.com/microsoft/winget-cli/releases/)



* superuser - 
[Is there a way to install Microsoft Store-exclusive apps without Store?](https://superuser.com/questions/1721755/is-there-a-way-to-install-microsoft-store-exclusive-apps-without-store)

* GitHub - 
[mjishnu / alt-app-installer](https://github.com/mjishnu/alt-app-installer)

* [microsoft / winget-cli](https://github.com/microsoft/winget-cli?tab=readme-ov-file#installing-the-client)


> [^1]. _**[Windows Package Manager 1.9.2411-preview Pre-release](https://github.com/microsoft/winget-cli/releases/){:target="_blank"}**_